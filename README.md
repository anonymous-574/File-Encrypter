CI/CD webhook test

# File-Encrypter
GUI program for Encrypting/Decrypting files using AES 256 bit 

### Description:
This Java GUI program is made using SWING and integration with Encryption/Decryption Algorithm <br>
The Algorith used here is the popular Advance Encryption Standard(AES)
I have used Cipher Block Chain method here 

and have integrated `SHA-256` hash algorithm for authentication here 
which uses SALT to avoid rainbow attacks to passwords here
`PBKDF2` function is used for computing this in our code 

When you run the program a window will open <br>

![front1](https://user-images.githubusercontent.com/44942652/147573068-19e123d5-49c6-43b9-bc85-c03ac4a262c5.jpg)

to select file click open <br>

![Menu1](https://user-images.githubusercontent.com/44942652/147573189-6112d263-778c-4ecc-b7dc-21ac59a08464.jpg)

in this menu select your file you want to Encrypt

![File](https://user-images.githubusercontent.com/44942652/147573628-b4cc2a62-ced3-430e-8c5d-e235b8c23dbe.jpg)

lets have this file encrypted

![Front2](https://user-images.githubusercontent.com/44942652/147573293-2864adc5-a424-4783-b897-286aad9304d4.jpg)

now Click on Encrypt

![Front3](https://user-images.githubusercontent.com/44942652/147573472-afb65c39-f323-4199-a868-74f95d1a75bd.jpg)

Now our file is Encrypted 

![File2](https://user-images.githubusercontent.com/44942652/147573549-53d02b73-bb33-4e0b-81a6-69e7dc3b55be.jpg)

now to decrypt it 

but if password is given wrong then

![Front4](https://user-images.githubusercontent.com/44942652/147573773-f8f89904-600f-49ea-946d-3b33fa55f0e9.jpg)

you wont be able to access it

![Front5](https://user-images.githubusercontent.com/44942652/147573871-abe8cdba-276c-4dcf-86e0-fb926b030e40.jpg)

but after entering correct you can

![Front7](https://user-images.githubusercontent.com/44942652/147573924-c332d058-9f30-4d17-be3a-fdead2464893.jpg)

Here's your file now

![File3](https://user-images.githubusercontent.com/44942652/147573997-5d328564-b0c0-43a3-8c48-2afe9897ba51.jpg)

That's all folks!

Note: This software is under development I am solving some bugs dont use it on important files 

#### &#128161; Techs & Tools

![](https://img.shields.io/badge/Code-Java-informational?style=flat&logo=data:image/svg%2bxml;base64,PHN2ZyByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48dGl0bGU+SmF2YSBpY29uPC90aXRsZT48cGF0aCBkPSJNOC44NTEgMTguNTZzLS45MTcuNTM0LjY1My43MTRjMS45MDIuMjE4IDIuODc0LjE4NyA0Ljk2OS0uMjExIDAgMCAuNTUyLjM0NiAxLjMyMS42NDYtNC42OTkgMi4wMTMtMTAuNjMzLS4xMTgtNi45NDMtMS4xNDlNOC4yNzYgMTUuOTMzcy0xLjAyOC43NjEuNTQyLjkyNGMyLjAzMi4yMDkgMy42MzYuMjI3IDYuNDEzLS4zMDggMCAwIC4zODQuMzg5Ljk4Ny42MDItNS42NzkgMS42NjEtMTIuMDA3LjEzLTcuOTQyLTEuMjE4TTEzLjExNiAxMS40NzVjMS4xNTggMS4zMzMtLjMwNCAyLjUzMy0uMzA0IDIuNTMzczIuOTM5LTEuNTE4IDEuNTg5LTMuNDE4Yy0xLjI2MS0xLjc3Mi0yLjIyOC0yLjY1MiAzLjAwNy01LjY4OCAwLS4wMDEtOC4yMTYgMi4wNTEtNC4yOTIgNi41NzNNMTkuMzMgMjAuNTA0cy42NzkuNTU5LS43NDcuOTkxYy0yLjcxMi44MjItMTEuMjg4IDEuMDY5LTEzLjY2OS4wMzMtLjg1Ni0uMzczLjc1LS44OSAxLjI1NC0uOTk4LjUyNy0uMTE0LjgyOC0uMDkzLjgyOC0uMDkzLS45NTMtLjY3MS02LjE1NiAxLjMxNy0yLjY0MyAxLjg4NyA5LjU4IDEuNTUzIDE3LjQ2Mi0uNyAxNC45NzctMS44Mk05LjI5MiAxMy4yMXMtNC4zNjIgMS4wMzYtMS41NDQgMS40MTJjMS4xODkuMTU5IDMuNTYxLjEyMyA1Ljc3LS4wNjIgMS44MDYtLjE1MiAzLjYxOC0uNDc3IDMuNjE4LS40NzdzLS42MzcuMjcyLTEuMDk4LjU4N2MtNC40MjkgMS4xNjUtMTIuOTg2LjYyMy0xMC41MjItLjU2OCAyLjA4Mi0xLjAwNiAzLjc3Ni0uODkyIDMuNzc2LS44OTJNMTcuMTE2IDE3LjU4NGM0LjUwMy0yLjM0IDIuNDIxLTQuNTg5Ljk2OC00LjI4NS0uMzU1LjA3NC0uNTE1LjEzOC0uNTE1LjEzOHMuMTMyLS4yMDcuMzg1LS4yOTdjMi44NzUtMS4wMTEgNS4wODYgMi45ODEtLjkyOCA0LjU2MiAwLS4wMDEuMDctLjA2Mi4wOS0uMTE4TTE0LjQwMSAwczIuNDk0IDIuNDk0LTIuMzY1IDYuMzNjLTMuODk2IDMuMDc3LS44ODggNC44MzItLjAwMSA2LjgzNi0yLjI3NC0yLjA1My0zLjk0My0zLjg1OC0yLjgyNC01LjUzOSAxLjY0NC0yLjQ2OSA2LjE5Ny0zLjY2NSA1LjE5LTcuNjI3TTkuNzM0IDIzLjkyNGM0LjMyMi4yNzcgMTAuOTU5LS4xNTMgMTEuMTE2LTIuMTk4IDAgMC0uMzAyLjc3NS0zLjU3MiAxLjM5MS0zLjY4OC42OTQtOC4yMzkuNjEzLTEwLjkzNy4xNjggMC0uMDAxLjU1My40NTcgMy4zOTMuNjM5Ii8+PC9zdmc+)
![](https://img.shields.io/badge/IDE-IntelliJ-informational?style=flat&logo=data:image/svg%2bxml;base64,PHN2ZyByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48dGl0bGU+SW50ZWxsaUogSURFQSBpY29uPC90aXRsZT48cGF0aCBkPSJNMCAwdjI0aDI0VjB6bTMuNzIzIDMuMTExaDV2MS44MzRoLTEuMzl2Ni4yNzdoMS4zOXYxLjgzNGgtNXYtMS44MzRoMS40NDRWNC45NDVIMy43MjN6bTExLjA1NSAwSDE3djYuNWMwIC42MTItLjA1NSAxLjExMS0uMjIyIDEuNTU2LS4xNjcuNDQ0LS4zOS43NzctLjcyMyAxLjExLS4yNzcuMjc5LS42NjYuNTU3LTEuMTEuNjY4YTMuOTMzIDMuOTMzIDAgMCAxLTEuNDQ1LjI3OGMtLjc3OCAwLTEuNDQ0LS4xNjctMS45NDQtLjQ0NWE0LjgxIDQuODEgMCAwIDEtMS4yNzktMS4wNTZsMS4zOS0xLjU1NWMuMjc3LjMzNC41NTUuNTU1LjgzMy43MjIuMjc3LjE2Ny42MTEuMjc4Ljk0NS4yNzguMzg5IDAgLjcyMS0uMTExIDEtLjM4OS4yMjEtLjI3OC4zMzMtLjY2Ny4zMzMtMS4yNzh6TTIuMjIyIDE5LjVoOVYyMWgtOXoiLz48L3N2Zz4=)
![](https://img.shields.io/badge/OS-Windows-informational?style=flat&logo=data:image/svg%2bxml;base64,PHN2ZyByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48dGl0bGU+V2luZG93cyBpY29uPC90aXRsZT48cGF0aCBkPSJNMCAzLjQ0OUw5Ljc1IDIuMXY5LjQ1MUgwbTEwLjk0OS05LjYwMkwyNCAwdjExLjRIMTAuOTQ5TTAgMTIuNmg5Ljc1djkuNDUxTDAgMjAuNjk5TTEwLjk0OSAxMi42SDI0VjI0bC0xMi45LTEuODAxIi8+PC9zdmc+)

![](https://img.shields.io/badge/Library-Swing-informational?style=flat&logo=<LOGO_NAME>&logoColor=white&color=2bbc8a)
![](https://img.shields.io/badge/Library-AWT-informational?style=flat&logo=<LOGO_NAME>&logoColor=white&color=2bbc8a)
![](https://img.shields.io/badge/Library-Cipher-informational?style=flat&logo=<LOGO_NAME>&logoColor=white&color=2bbc8a)
![](https://img.shields.io/badge/Library-Security-informational?style=flat&logo=<LOGO_NAME>&logoColor=white&color=2bbc8a)
![](https://img.shields.io/badge/Library-io-informational?style=flat&logo=<LOGO_NAME>&logoColor=white&color=2bbc8a)
