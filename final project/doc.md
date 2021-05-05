# Build a Minecraft Server
![Minecraft](./pics/minecraft-title.webp)

## Table of content here
- [Build a Minecraft Server](#build-a-minecraft-server)
  - [Table of content here](#table-of-content-here)
  - [Project Description](#project-description)
  - [Requirements](#requirements)
  - [Setting Up The Minecraft Server on Local PC (Ubuntu)](#setting-up-the-minecraft-server-on-local-pc-(ubuntu))
    - [Local PC specifications](#local-pc-specifications)
    - [Download and install Java Development Kit](#download-and-install-java-development-kit)
    - [Download and install Minecraft](#download-and-install-minecraft)
    - [Download and setup Minecraft server](#download-and-setup-minecraft-server)
      - [Create a Game folder](#create-a-game-folder)
      - [Configure server files](#configure-server-files)
    - [Run the game](#run-the-game)
  - [Difficulties Encountered](#difficulties-encountered)
  - [Work Cited](#work-cited)

## Project Description
In this project, I am creating a Minecraft Server hosted on a Local machine. The application must meet the following requirements:
* Must provide a server room to play.
* Able to play with other people over same network.

## Requirements
The project requires the use of a PC. I am using the following specifications:

* OS: Ubuntu 20.04.2 LTS
* RAM: 8 GB
* CPU: Intel i5

## Setting Up The Minecraft Server on Local PC (Ubuntu)
### Local PC specifications

Inorder to run Minecraft's server the local PC must have minimum following specifications:

* RAM: 512mb
* CPU: Intel Pentium 4
* Network download speed: 3 Mbit/s 
* Network upload speed: 2 Mbit/s 
* HDD: 2 GB empty space
(5GB if you are doing frequent backups) 

With this specification, server will be able to handle 1-2 players. As the specifications are upgraded, the server will be able handle more players. 

### Download and install Java Development Kit

The Minecraft version that is used here is developed using Java programming language. So, we have to download [JDK](https://en.wikipedia.org/wiki/Java_Development_Kit) .

Goto [Amazon Coretto 16 JDK](https://docs.aws.amazon.com/corretto/latest/corretto-16-ug/downloads-list.html), download JDK for linux x64 deb package.

![JDK](./pics/jdk.png)

After that, the file will begin to download. After the download is complete double click the .deb file.

![JDK deb](./pics/jdk-1.png)

A window will appear. Click install to install the JDK. After the installation, close the opened window.

![JDK install](./pics/jdk-2.png)

The JDK is now installed.

### Download and install Minecraft

1. Goto the [TLauncher](https://www.minecraft.net/en-us/store/minecraft-java-edition)
2. Click on `Download TL`
![Tlauncher](./pics/tlauncher.png)
3. Click on Linux
![Tlauncher site](./pics/tlauncher-site.png)
A file will begin to download. After the download
4. Extract the downloaded zip file
![Tlauncher-1](./pics/tlauncher-1.png)
5. Goto the extracted folder from terminal
![Tlauncher-2](./pics/tlauncher-2.png)
6. Run the following command to execute the .jar file<br>
  `sudo java -jar TLauncher-x.xx.jar`<br>Where `x's` are the version of the file you download.

    ![Tlauncher-3](./pics/tlauncher-3.png)
    
    A process will begin

    ![Tlauncher-4](./pics/tlauncher-4.png)

  * The `sudo` gives admin priviliges, so that we do not encounter any permission denied issue.<br>
  * The `java` invokes the JDK we installed.<br>
  * The `-jar` argument here is the type of the file we are adding, to explicitly tell what to compile and Java compiler knows how to handle .jar file.<br>
  * The `Tlauncher-x.xx.jar` is the file name with extension.<br>


7. The TLauncher will appear. Set your username, then click on `Install` to begin downloading the game files and install them.

    ![Tlauncher-5](./pics/tlauncher-5.png)

    The download will begin.

    ![Tlauncher-6](./pics/tlauncher-6.png)


8. After the download is complete, a window will appear. Click on `OK`
![Tlauncher-7](./pics/tlauncher-7.png)

9. Now click on `Enter the game` to launch Minecraft.
  ![Tlauncher-8](./pics/tlauncher-8.png)
  Minecraft will appear.
  ![Tlauncher-9](./pics/tlauncher-9.png)

10. Minimize the window for now, will come back later after we create the server.

### Download and setup Minecraft server

Goto [Minecraft official server download page](https://www.minecraft.net/en-us/download/server/), and download minecraft_server.x.x.x.x.jar file (x can be any number).

![Server](./pics/server.png)

A .jar file will be downloaded


#### Create a Game folder

1. Create a new folder on any drive.
2. Like For example ~:Home\Downloads\Server\
3. Copy and paste the downloaded jar, in the created folder.
![Server-1](./pics/server-1.png)

### Configure server files

1. Open the terminal, and cd to the folder where the download .jar file is.
![Server-2](./pics/server-2.png)

2. Run this command to execute the .jar file<br>
`java -Xmx1024M -Xms1024M -jar minecraft_server.x.xx.x.jar nogui `<br>
Where `x's` are the file version.
![Server-3](./pics/server-3.png)

  * `-xmx1024M` and `-xms1024M` is the argument that is given the the .jar file.
  * `minecraft_server.x.xx.x.jar` is the file name
  * `nogui` part is optional, one can leave if he/she want's the the server to run in GUI instead of terminal. I used `no gui` here.  

3. The server will start and you will see this message. 
![Server-4](./pics/server-4.png)
 The server jar file will automatically create necessary configurations file.


3. Have to make some modifications, before the server is of any use.
4. Open the `eula.txt` file in the directory where the .jar file is.
![Server-5](./pics/server-5.png)


5. Replace `eula=false` with `eula=true` and save the eula.txt file . The purpose of doing this, is of agreeing with the terms and condition.

![Server-6](./pics/server-6.png)

6. Open `server.properties` file. 

7. Change `online-mode=true` to `online-mode=false`

![Server-8](./pics/server-8.png)

6. Relaunch the server jar file again.

7. If `done` appears on terminal, it means the server is successfully created. Keep this terminal opened, as long as the game have to be played.

8. Goto the settings > WiFi > Click on the gear icon of your connected network . Copy the ipv4 address. The ipv4 address is needed so that people with other devices on same network, can find this server over LAN.

![Server-14](./pics/server-14.png)

### Run the game

1. Open the minimized game and goto the multiplayer tab.
![Game](./pics/game.png)

2. Paste the copied ipv4 address and then click on `Join Server`
![Server-15](./pics/server-15.png)

The Game will appear on a server world!

![Minecraft-server](./pics/minecraft-server.png)

## Difficulties Encountered 

**Minecraft download issue:**
There are many version of minecraft available like Windows 10 Edition, Pocket edition,Java version and even there is an online browser based Minecraft. So, after researching found that most tutorials availabe are of Java version.

I also had issue from where to download Minecraft. I head over to the official site, choose Minecraft Java and linux edition and it was a paid one. Then I found, there is also a moded version as TLauncher. So, I downloaded that.

**Minecraft Server Choose:**

There are some options online to make Minecraft server. Like for example, we can choose a hosting provider, we can also use AWS for minecraft server, or there are online options where have to make an account on some site and make server there. All of these are pre-made options.So, after researching, I found that I can myself download and configure the server, which is downloaded from official minecraft site and comes in a .jar package.

**Java Download issue:**
I was not sure about what Java version to download, as there is JDK and a Java SE.Some tutorial said to download one while other said to download the other.In the end, I downloaded JDK, as I read that it also comes with what Java SE offers.

Next comes the part of downloading JDK. There are bunch of options availabe online. There are many open vendors of JDK. Had too research thoroughly to download the one which will work. I downloaded the Amazon Coretto 16 JDK which was the latest there. The reason to choose Coretto over the others is because it had a ubuntu support and was easy to install. Additionally, Amazon uses this JDK for it's Java technologies. So, this way this gave no issue.

## Work Cited

iDTech. “How to Make a Minecraft Server | 12 Steps to Set Up & Host Your Own Free Server.” iDTech, iDTech, 02 Feb. 2017, https://www.idtech.com/blog/creating-minecraft-server. 


“YouTube” YouTube - How to Create a Minecraft Server for FREE for Tlauncher | WITHOUT ATERNOS, SERVER.PRO, https://www.youtube.com/watch?v=qYgJq6OPpo8&t=217s 

“What Is JDK?” JDK, https://en.wikipedia.org/wiki/Java_Development_Kit. 