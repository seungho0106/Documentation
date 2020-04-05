---
layout: default
title: Configuring CheckStyle
nav_order: 3
---

# Configuring CheckStyle
{: .no_toc }


---

[CheckStyle](https://checkstyle.sourceforge.io/) is a tool to help developers write Java code that adheres to a particular coding convention. CheckStyle analyzes the code to check for certain rules, such as formatting and code layout, and alerts any issues to the developer. As a result, projects that utilize CheckStyle have easily-readable and well-formatted code.

Each Checkstyle configuration file (.xml) has their own unique rulesets defined. Developers can choose to use the bundled configuration files or customized configuration files.

This section will examine how to integrate CheckStyle into your IntelliJ IDEA and run CheckStyle tests against your code.

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Installing CheckStyle-IDEA Plugin
This instruction set will install the CheckStyle-IDEA plugin needed to run CheckStyle on IntelliJ IDEA.

1. **Open** IntelliJ IDEA to a new project.

2. **Click** on \[IntelliJ IDEA\] > \[Preferences\] from the toolbar at the top of your screen. A new "Preferences Window" should appear.<br>
![Toolbar 1](https://github.com/seungho0106/Documentation/blob/gh-pages/assets/images/version-control/vc4.png?raw=true "Toolbar 1")<br>

3. In the "Preferences Window", **click** on \[Plugins\] on the left side. **Check** \[Marketplace\] is highlighted at the top of the "Preferences Window", and **type** `CheckStyle-IDEA` in the search bar.
![Marketplace](https://github.com/seungho0106/Documentation/blob/gh-pages/assets/images/checkstyle/checkstyle01.png?raw=true "Marketplace"){: style="width: 90%" }

4. **Click** on \[Install\] and **wait** for the download to finish.
![Install CheckStyle](https://github.com/seungho0106/Documentation/blob/gh-pages/assets/images/checkstyle/checkstyle02.png?raw=true "Install CheckStyle"){: style="width: 100%" }

5. **Restart** the IntelliJ IDEA by **clicking** on \[Restart IDE\].
![Install CheckStyle](https://github.com/seungho0106/Documentation/blob/gh-pages/assets/images/checkstyle/checkstyle03.png?raw=true "Install CheckStyle"){: style="width: 100%" }

6. After the IntelliJ IDEA has reloaded, **navigate** to \[Preferences\] > \[Plugins\] and **click** on \[Installed\].
![Installed](https://github.com/seungho0106/Documentation/blob/gh-pages/assets/images/checkstyle/checkstyle04.png?raw=true "Installed")

7. **Ensure** CheckStyle-IDEA is enabled with a check mark. You should also see [CheckStyle] near the bottom-left corner of the "Main Window".
![CheckStyle Enabled](https://github.com/seungho0106/Documentation/blob/gh-pages/assets/images/checkstyle/checkstyle05.png?raw=true "CheckStyle Enabled"){: style="width: 100%" }
![Toolbar 2](https://github.com/seungho0106/Documentation/blob/gh-pages/assets/images/checkstyle/checkstyle06.png?raw=true "Toolbar 2"){: style="width: 100%" }

---

## Running CheckStyle Tests
Let's try running a few tests to see how clean our code is. We will first configure which CheckStyle rules to enforce for the current project. 

1. **Navigate** to \[IntelliJ IDEA\] > \[Preferences\] > \[Other Settings\] > \[Checkstyle\].

2. Under 'Configuration File', **click** the checkbox next to the desired CheckStyle configuration file. **Click** on \[Apply\] > \[OK\] to **save** the settings and **close** the "Preferences Window".
Note: If you wish to add a customized CheckStyle configuration file, click on \[+\] under 'Configuration File'.

3. **Download** the [CheckStyleTest.java](url) file and add it to your project directory. The file should appear on the left side of the IntelliJ IDEA.

4. **Open** the CheckStyleTest.java file by double-clicking on the file name. Once you select the file to test, **run** the tests by clicking on \[CheckStyle\] at the bottom, then the green play button. CheckStyle will now begin to analyze the selected file.

5. After analysis is complete, CheckStyle will inform you of all the violated standard checks. For CheckStyleTest.java, there should be a few errors including 'LocalVariableName'.
Note: The official documentation for standard checks can be found [here](https://checkstyle.sourceforge.io/checks.html).

Now you can use CheckStyle to detect any stylistic errors and write consistent code throughout your project.