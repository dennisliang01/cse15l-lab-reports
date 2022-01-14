# Week 2 Lab Report
January 14th, 2022

Last Updated: January 13th, 2022 by Dennis Liang

---


## Installing VScode
1. Go to https://code.visualstudio.com/
![Image](Screenshot 2022-01-13 150715.png)
2. Download the appropriate version of Visual Studio Code (VSCode) for your computer
3. After opening VSCode, it should look similar to image below


## Remotely Connecting
1. To securely access computer over the internet we need to use Secure Shell (SSH). Download and intall OpenSSH from [here](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)
2. Go to https://sdacs.ucsd.edu/~icc/index.php to check your login information
3. Open a terminal in VSCode and enter your login information as asked
![Image](Screenshot 2022-01-13 153301.png)
4. You will be prompted to confirm you want to conintue connecting, enter "yes"
5. Then enter your password. Keep in mind that your password will not show up on the screen.
![Image](Screenshot 2022-01-13 153556.png)
6. Congrulation you have just logged in!


## Trying Some Commands
Below are some commands to try out. The terminal is a command line interface as oppose to the graphical interface we are used to using.

mkdir: make directory
```
mkdir firstDirectory
```
ls: list files
```
ls
```
cd: change directory
```
cd firstDirectory
```

Your results should be something like the follwing
![Image](Screenshot 2022-01-13 155457.png)

To exit you can use either commmand
* ctrl-d
* exit


## Moving Files with scp
When you log in, you are using the ieng6 computer. To transfer file from your computer to ieng6, you need to use the scp command.


## Setting an SSH Key

## Optimizing Remote Running






