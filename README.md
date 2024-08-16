# 🎮 Minecraft Plugin Template 🎮
This repository provides a template for creating a Minecraft plugin using the Spigot API (and compatible with Paper). It includes a basic outline of the file structure, a template README file, and other helpful resources.

## Table of Contents
### 1. [Features](#-features-)
### 2. [Quickstart Guide](#-quickstart-guide-)
### 3. [Maven Setup (Optional)](#%EF%B8%8F-maven-setup-optional-%EF%B8%8F)
### 3. [README.md Template](#-readmemd-template-)
### 4. [Licensing Information](#-licensing-information-)

---

# ⭐ Features ⭐
* ## Plugin Repo
  * Contains basic Minecraft plugin repository structure
  * `plugin.yml` file and `config.yml` file
  * Compatible with both Spigot and Paper
* ## .gitignore File
  * Excludes many different files related to Minecraft plugin development
  * Support for IntelliJ IDEA, NetBeans, Eclipse, and VS Code
  * Excludes Maven files
* ## Template README.md File
    * Five customizable sections: 
      * Features
      * Commands
      * Config
      * Contribution
      * License
    * All you need to do is update the placeholder text with your plugin's information

---

# ✅ Quickstart Guide ✅
<details>
  <summary><h3>Step 1: Create your repository</h3></summary>

  ### Part 1
  On the main page of this repository, click `Use this template` which is located above the list of files.<br>
  Then select `Create a new repository`.<br>
  <img src="https://github.com/atlaska826/repo-images/blob/main/minecraft-plugin-template/create-template/Template.png" title="Use this template" alt="Use this template" width="30%">

  ### Part 2
  Use the owner dropdown to select which account you want to own the repository.<br>
  Give your repository a name.
  If you'd like, you can also include a description.<br>
  <img src="https://github.com/atlaska826/repo-images/blob/main/minecraft-plugin-template/create-template/Name.png" title="Owner, name, description" alt="Owner, name, description" width="60%">

  ### Part 3
  Set your repository's visibility.<br>
  <img src="https://github.com/atlaska826/repo-images/blob/main/minecraft-plugin-template/create-template/Visibility.png" title="Visibility" alt="Visibility" width="40%">

  ### Part 4
  Select `Create repository from template`.<br>
  <img src="https://github.com/atlaska826/repo-images/blob/main/minecraft-plugin-template/create-template/Create.png" title="Create repository from template" alt="Create repository from template" width="30%">
    
</details>

<details>
 <summary><h3>Step 2: Change package name</h3></summary>
  
 While you can change your package name in your IDE, you can also do it in GitHub using their web editor. Below are the steps you can take to change your package name on GitHub before you clone the repository. 
  
 ### Part 1
 Navigate to the `src/main` file in your new repository.<br>
 <img src="https://github.com/atlaska826/repo-images/blob/main/minecraft-plugin-template/package-name-change/Main.png" title="src/main" alt="src/main" width="30%">
  
 ### Part 2
 Change the `github.com` in your URL to `github.dev` to open up the web editor.<br>
 <img src="https://github.com/atlaska826/repo-images/blob/main/minecraft-plugin-template/package-name-change/URL1.png" title="github.com" alt="github.com" width="20%"><br>
 <img src="https://github.com/atlaska826/repo-images/blob/main/minecraft-plugin-template/package-name-change/URL2.png" title="github.dev" alt="github.dev" width="20%">
  
 ### Part 3
 In the editor, navigate to `src/main --> java`.<br>
 <img src="https://github.com/atlaska826/repo-images/blob/main/minecraft-plugin-template/package-name-change/FilePath.png" title="File Path" alt="File Path" width="30%">
  
 ### Part 4
 You should now be in `java/io/atlaska826/templateplugin`. Rename your package by right-clicking on each part of the package and selecting rename. *You **cannot** use capitals in your package name.*
  
 **Example:** `java/io/atlaska826/templateplugin` --> `java/com/yourname/pluginname`.
  
 ### Note
 Remember to also change your package in the [TemplatePlugin.java](src/main/java/io/atlaska826/templateplugin/TemplatePlugin.java) file and the [plugin.yml](src/main/resources/plugin.yml)!
  
</details>

<details>
 <summary><h3>Step 3: Setup your project</h3></summary>
 
 ### Part 1
 Before you begin, you'll want to navigate to the directory you want to make your repository in. In the IDE of your choosing, open the terminal, and use the `cd` command to get to the directory you want to create your project folder in. You can also use the built-in terminal on your computer to complete this step.
 
 For example if you store all your projects in a folder called `IntelliJ Projects`, then you would want to navigate to that folder. 
 
 
 ### Part 2
 Start about by cloning your newly made repository to your local device. In whatever terminal you have open, type the following command:
 ```
 git clone <your-repository-url>
 ```
 If you did not use the terminal in your IDE, you will now want to open your project in the IDE of your choosing.
 
 ### Part 3
 **At certain times, I've found that doing this step can cause issues for those who wish to utilize Maven in their project. I would recommend completing the steps to add support for Maven to your project prior to completing this next part.**
 
 Once you have cloned your repository on your local device, you will need to connect your project to your repository on GitHub so that you can push changes to it. In your **IDE's** terminal, make sure you are in the root directory of your project and then type in the following command: 
 ```
 git remote add origin <your-repository-url>
 ```
 You can verify that the remote has been added by typing in the following command:
 ```
 git remote -v
 ```
 
</details>

---

# ⚙️ Maven Setup (Optional) ⚙️ 
This section will detail Maven Setup for IntelliJ only since it is the IDE I usually use and am familiar with.
<details>
 <summary><h3>Step 1: Add Maven support</summary>
 
 ### Part 1
 With your project open, right-click on the project folder in your project tool window (the thing on the left side of your screen). In the dropdown, find the button labeled `Add Framework Support...` and click it. 
 
 ### Part 2
 In the window that pops up, select the checkbox labeled `Maven`. Then click `OK`. IntelliJ will generate the default Maven layout as well as a `pom.xml` file.
  
</details>

<details>
 
 Since the Spigot API works fine on Paper servers, this tutorial will focus on building with Spigot. If you would like to develop with the Paper API, please see this [link](https://docs.papermc.io/paper/dev/project-setup).
 <summary><h3>Step 2: Setup your pom.xml file</summary>
 
 ### Part 1
 In the newly created `pom.xml` file, you will need to specify a `groupId`. I would recommend your `groupId` be the same as your package name. For example, the `groupId` for this template plugin would be `io.atlaska826`. 
 
 ### Part 2
 Under the `<version>` tags in your `pom.xml` file, you'll want to add the following code:
 ```
 <repositories>
    <repository>
        <id>spigot-repo</id>
        <url>https://hub.spigotmc.org/nexus/content/repositories/snapshots/</url>
    </repository>
 </repositories>

 <dependencies>
    <dependency>
        <groupId>org.spigotmc</groupId>
        <artifactId>spigot-api</artifactId>
        <version>1.19.4-R0.1-SNAPSHOT</version>
        <scope>provided</scope>
    </dependency>
 </dependencies>
 ```
 You can always change you API version to fit whatever your needs are. If you do change you API version to be something other than 1.19, make sure you update the `api-version` in your `plugin.yml` file.
 
 ### Part 3
 Load your Maven changes by clicking the Maven icon that appears on the right side of the editing window (pictured below).
 <img src="https://github.com/atlaska826/repo-images/blob/main/minecraft-plugin-template/maven-setup/MavenButton.png" title="Maven Icon" alt="Maven Icon" width="20%">

</details>

<details>
 <summary><h3>Step 3: Compiling your plugin</summary>
 
 ### Part 1
 On the right side of your IntelliJ window, you should see a tab labeled `Maven`. Click on it. 
 
 ### Part 2
 Use the dropdown arrows next to your plugin's name in the Maven tab and expand the `Lifecycle` tree.
 
 ### Part 3
 In the `Lifecycle` tree, double-click the button labeled `package`. Your plugin will now be compiled in a folder named `target` under your project root. 
 
 ### Note
 If you would like to specify your `.jar` file's name and output directory, add the following code about the `<repositories>` tag in your `pom.xml` file:
 ```
 <build>
     <finalName>TemplatePlugin</finalName>
     <plugins>
         <plugin>
             <groupId>org.apache.maven.plugins</groupId>
             <artifactId>maven-jar-plugin</artifactId>
             <version>3.3.0</version>
             <configuration>
                 <outputDirectory>/Path/To/Preferred/Directory</outputDirectory>
             </configuration>
         </plugin>
     </plugins>
 </build>
 ```
 You can change the value in the `<finalName>` tags to change your `.jar` file's name. The directory should be pretty self-explanatory.
 
</details>
 
---

# 📘 README.md Template 📘
### Instructions:
1. Copy the text below
2. Paste it into your project's `README.md` file
3. Edit the information as needed

```
# Plugin Name Here
Plugin description here.

## ⭐ Features ⭐
### Feature 1
* Description
### Feature 2
* Description
### Feature 3
* Description

## ⌨️ Commands ⌨️
### `commandOne-name`:
* Function:
* Permission:
### `commandTwo-name`:
* Function:
* Permission:
### `commandThree-name`:
* Function:
* Permission:

## ⚙️ Config ⚙️
Insert information for plugin configuration here.

## 📥 Contribution 📥
Insert information on how to contribute to your plugin here.

## 📝 License 📝
Insert license information here.
```

---

# 📝 Licensing Information 📝
### ‼️ IMPORTANT: PLEASE READ ‼️
While this template repository is licensed under the MIT license, both the Spigot and Paper APIs are licensed under the GNU General Public License v3.0 license. As such, your plugin may need to be licensed under the GPL v3.0 license. However, that is not always the case. For more information about each APIs licensing, please see the links below. 

Link to [Spigot License](https://github.com/SpigotMC/Spigot-API/blob/master/LICENCE.txt)<br>
Link to [Paper License](https://github.com/PaperMC/Paper/blob/master/LICENSE.md)
##
Copyright © 2024 Atlas Mallams

This repository is licensed under the MIT License.<br>
For more information, please see [LICENSE](LICENSE).

