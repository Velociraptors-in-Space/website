---
layout: page
title: Setup
description: "This document outlines the setup procedures that enable us to work together on the robot code."
---

This document outlines the setup procedures that enable us to work together on the robot code. Please follow the procedures as closely as you possible can, and contact your programming head if you run into an issue.

# Java

We program in the Java language, so you need to install the Java Development Kit in order to be able to program the robot.

## Download

Go to http://jdk.java.net/11/ and download the correct Java package for your system.

## Install - Windows

Unpack the `openjdk-11.x.x_windows-x64_bin.zip` file and move the `jdk-11.x.x` folder into your Java directory. (Usually `C:\Program Files\Java`)

### Environment Variable

In order for Java to integrate well with other programs, the operating system needs to know where Java is located on the system. 

1. To do this, search `environment variables` in the start menu and open the first option. 

2. Then, at the bottom right of the window that opens, click `Environment Variables...`

3. If the `JAVA_HOME` variable already exists in the `System variables` section, then click the `Edit...` button. Otherwise, click the `New...` button.

4. The variable name should be `JAVA_HOME`. 

5. The variable value should be the path to your Java installation (including the JDK-11 folder). If you followed the instructions exactly, then your Java installation path should be `C:\Program Files\Java\jdk-11.x.x`. 

## Install - Mac & Linux

1) ???

2) Profit

Unfortunately, I do not know how to manually install Java on Unix machines. Good luck!

# Visual Studio Code

We need a nice interface to program with, because the command line is hard. The IDE (Integrated Development Environment) FIRST suggests we use is Visual Studio Code, which is developed by Microsoft. Download the installer appropriate for your system from https://code.visualstudio.com/#alt-downloads and run the installer to install VS Code.

# Java Extension Pack

Visual Studio Code is not configured to run Java by default, even though you installed Java on to your system. In order to make VS Code work with Java, you need to install the Java Extension Pack.

1. To do this, open the extensions side-bar in VS Code (this is the 5th icon on the side-bar on the left of the IDE).

2. Search for `java`.

3. Click `install` on the `Java Extension Pack`.

4. Move on to the next section so you can get all the extensions installed before Java finishes downloading and installing.

# WPILib Extension

There are no built-in Java classes and methods for controlling a robot, so without extra packages, we would need to create a whole slew of classes to do simple things like control motors. 

In addition, the RoboRio - the Arduino-like device that controls our robot - needs the Java files in a specific format (`JAR`- java archive) in order to be able to run our code. 

The WPILib VSCode extension takes care of both of these problems. Firstly, it includes a number of packages that let us easily use the functions of the robot. Secondly, it uses the Gradle build system to build the `JAR` that runs the robot.

1. Download the WPILib extension from https://github.com/wpilibsuite/vscode-wpilib/releases. (Ask your programming head for the correct version!)

2. Click the 3-dot menu button at the top right of the extensions panel.

3. Click `Install from VSIX...`

4. Find the `VSIX` file you downloaded before using the File Explorer window that just opened and click `Install`.

5. Once the extension is installed, it will give you a message on the bottom right corner of the IDE. Click `Restart`when it appears.

# Git

In order for multiple people to work together on the robot code, there needs to be some method of sharing and organizing the code in real time. There also needs to be a way of tracking who wrote what, so that people will be responsible for the code they write.

The system we use for this purpose is Git, which is a protocol used by many companies and open-source projects. Our Git provider is [GitHub](github.com). Git is a lot like Google Drive, in that it has files and shows the changes that people make on them. The difference between Git and Google Drive is that Git does not actually store the files themselves. It stores everything as changes, which are grouped together into commits. This way, instead of storing files in a folder, Git stores everything as changes to the content of that folder. Creating a file, renaming a file, deleting a file, and changing a word in a file are all changes that can be part of commits. 

In order to use Git, you must install the Git protocol on your computer, which will add commands that VS Code will use.

1. To install Git, download the correct installer for your system at https://git-scm.com/downloads. 

2. Run the installer.

3. During the installation process, make sure to `add git to PATH variable` if you are asked whether the installer should. Also, set the default Git editor to VS Code if you have the option to. All the other options should be left as default.

# Download The Code

Now that you have everything installed, you can download the code to your computer. We can use the Git protocol to do this, and VS Code has built in Git support to help you with that.

1. Press `Ctrl-Shift-P` (or the Unix equivalent) on your computer to open the command palette.

2. Type `Git Clone` and press enter.

3. In the small box that appears, enter `https://github.mcrobotics.ca/code` as the repository URL.

4. Select a location to download the repository to. Git will automatically generate a folder called `code` for you.

5. When a message pops up in the bottom right corner, press `Yes` to open the repository you just downloaded.

# Start Programming

Congratulations! You completed the setup of our programming environment. Move onto the next lesson or talk to your programming head.
