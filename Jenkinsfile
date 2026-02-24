node {
    try {
        stage('Checkout') {
            // This is usually automatic when you use "Pipeline script from SCM"
            // but it's good to be explicit sometimes
            checkout scm
        }

        stage('Build') {
            sh '''
                echo "Building Java project..."
                echo "Current directory: $(pwd)"
                echo "Workspace contents:"
                ls -la
                
                cd "Password Protection" || { echo "Directory 'Password Protection' not found"; exit 1; }
                
                mkdir -p build
                javac -d build src/*.java
                
                if [ $? -eq 0 ]; then
                    echo "Build successful"
                else
                    echo "Compilation failed"
                    exit 1
                fi
                
                echo "Compiled classes:"
                ls -R build
            '''
        }

        stage('Test') {
            sh '''
                set -e  # exit on any error
                
                echo "Running JUnit tests for File-Encrypter..."
                cd "Password Protection" || { echo "Cannot cd to Password Protection"; exit 1; }
                
                # Always clean any potentially corrupted JUnit jar
                rm -f junit-platform-console-standalone*.jar
                
                echo "Downloading fresh JUnit Platform Console Standalone..."
                curl -L --fail --show-error -o junit-platform-console-standalone.jar \
                    https://repo1.maven.org/maven2/org/junit/platform/junit-platform-console-standalone/1.10.2/junit-platform-console-standalone-1.10.2.jar
                
                # Quick sanity check
                if [ ! -s junit-platform-console-standalone.jar ]; then
                    echo "ERROR: Downloaded JUnit JAR is empty or missing"
                    exit 1
                fi
                
                echo "Downloaded JUnit JAR size:"
                ls -lh junit-platform-console-standalone.jar
                
                # Compile tests
                mkdir -p test-build
                javac -cp "junit-platform-console-standalone.jar:build" \
                      -d test-build test/*.java
                
                echo "Compiled test classes:"
                ls -R test-build
                
                # Run tests
                java -jar junit-platform-console-standalone.jar \
                    --class-path "build:test-build" \
                    --scan-classpath \
                    --reports-dir=../test-reports
                
                echo "JUnit tests completed"
            '''
        }

        stage('Package') {
            sh '''
                echo "Creating JAR artifact..."
                cd "Password Protection" || exit 1
                
                mkdir -p ../artifacts
                
                # Simple JAR with all compiled classes
                jar cfe ../artifacts/FileEncrypter.jar Main -C build .
                
                echo "Artifact created:"
                ls -lh ../artifacts/FileEncrypter.jar
            '''
        }

        echo "Pipeline completed successfully!"
    } catch (Exception e) {
        echo "Pipeline failed: ${e.message}"
        currentBuild.result = 'FAILURE'
        throw e
    } finally {
        // Optional: archive test results / artifacts even on failure
        archiveArtifacts artifacts: 'artifacts/*.jar', allowEmptyArchive: true
        junit 'test-reports/*.xml', allowEmptyResults: true
    }
}
