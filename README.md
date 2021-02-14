# Installing VSCode, Python and Java on a Jetson Nano

## Installing VSCode and Python

1. First, log into your Jetson Nano device. Once logged in, you will need to connect to the internet before downloading anything from the internet. Choose a wifi connection by clicking on the wifi icon on the top right corner of the toolbar:

![](resources/wifiIcon.png)

You will then be prompted to select the name of the wifi connection to connect to and enter the wifi connection's password:

![](resources/wifiSelection.png)



2. Next, open a <i>Terminal Window</i> -- a special program used for issuing computer commands to your machine.  The commands issued will be commands that download programs (VSCode, Python and Java) from the internet. 

To open a Terminal window, simply double-click on the "Terminal" shortcut on the desktop:

![](resources/openingTerminal.png)

This will open a purple "Terminal Window" with a cursor.  This will be where we will input our download commands:

![](resources/openTerminal.png)

3. Now, we will run 3 commands that will download and install VSCode and Python.
Copy the following command, and paste it into the Terminal window, and press "ENTER". (you can also type the command into the Terminal by hand, but this can be error-prone and the command needs to be typed in verbatim.). 
```bash
git clone https://github.com/JetsonHacksNano/installVSCode.git
```

After pressing "ENTER", the Terminal will output information explaining what action it performed. It will look as follows:
![](resources/cloneRepo.png)


Now, copy and paste the second command.  Then, hit "ENTER".  This command (`cd`) "changes directories" into the 'installVSCode' directory.  In otherwords, you are opening the 'installVSCode' folder to access the files in it:
```bash
cd installVSCode
```

You will not see any output on the terminal, but the location on your Terminal window will change to 'installVSCode', because you are now inside of a folder called 'installVSCode':

![](resources/cd.png)

Lastly, copy and paste the following command.  It simply runs a "shell script" file called 'installVSCodeWithPython.sh' that handles the installation of VSCode and Python for us.  (NOTE: When promted, enter your Jetson Nano's password.  You're asked for it because system files that require admin access will be updated). This command may take up to three minutes to finish executing:
```bash
sudo ./installVSCodeWithPython.sh
```

![](resources/runShell.png)

Once the Terminal screen stops outputting information, search for 'VSCode' in your computer:
 
![](resources/vscodeInstalled.png)



Lastly, go back to the terminal and type the `clear` command to erase all of the output generated by the previous command: 
```bash
clear
```

Then, run the following command to verify that Python was installed:
```bash
python --version
```

Your terminal screen should output information on the version of python:
![](resources/pythonVersion.png)

That's it! You've downloaded VSCode and Python onto your Jetson Nano.


# Installing Java

1). Open a Terminal window and run the following command to download Java. When prompted, enter your password.  You will also be asked if you would like to accept the installation location of the software -- press 'Y' and "ENTER" to continue:
```bash
sudo apt install default-jdk
```

Your output will look as follows:

![](resources/javaOutput.png)


2). Java should now be installed.  To verify, run the following command to show details about the version of Java that was installed:
```bash
java -version
```

The output should look similar to the following (simply showing details about the installation):

![](resources/javaVersion.png)


That's it -- you installed Java on your Jetson Nano!
