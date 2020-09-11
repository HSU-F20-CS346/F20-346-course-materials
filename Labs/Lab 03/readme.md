# Lab 3 - Intro to wireshark
In this lab, we will use wireshark to examine packets being sent between your local machine, your virtual machine, and the Internet.  Begin by [downloading wireshark](https://www.wireshark.org/download.html).  Note that you may be required to restart your computer for the installation to complete.

Once wireshark is installed, [watch this introductory video](https://www.youtube.com/watch?v=r0l_54thSYU).  It does a pretty good job explaining the basics of the software.

## Running the Chat Server on your Virtual Machine
After completing the video, boot up your VM.  If you haven't done so in a while, issue the following commands to update your machine:

```
sudo apt update
sudo apt upgrade
```

If a kernel update was applied, you will need to **_restart your VM_**.  You can tell if this is needed by looking for a line near the bottom of the output that references ```/boot/vmlinux....```.  Should you need a reboot, do so now using ```sudo reboot```.  

Once you have a freshly updated system, you will next need to install the [.NET framework for Linux](https://docs.microsoft.com/en-us/dotnet/core/install/linux-ubuntu).  You should be running Ubuntu 20.04, so follow the instructions under that header.  If you are SSHing into your VM, you should be able to easily copy and paste these commands into your SSH terminal (i.e. [Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) on Windows).

Now that we have the .NET framework installed, we are going to download and the chat server.  Issue the following commands in your terminal:

```
cd 
sudo apt install zip unzip
wget https://github.com/HSU-F20-CS346/chat-server/releases/download/v1.0.0/chatserver.zip
unzip chatserver.zip
```

This should download and extract the chat server into your home directory.  Now, we can finally run the server:

```
cd chatserver
dotnet ChatServer.dll
```

If successful, you should see messages about an Authenticator, Receiver, and Broadcasters waiting for connections.

## Running the Chat Client on your Host Machine
Next, [download the chat client](https://github.com/HSU-F20-CS346/chat-server/releases/download/v1.0.0/chatclient.zip) on your host machine.  Be sure to extract the ZIP file to an actual folder.  On Windows, double click ```ChatClient.exe``` or on OSX / Linux execute ```dotnet ChatClient.dll``` in a terminal.  Note that Windows users may get a message about an untrusted executable.  If that message screen appears, click the "More Info" button and allow the application to run.  

At this point, it would be a good idea to have wireshark start listening for network traffic.  Depending on how you have your VM configured, you may have to play around with the listening interface inside of wireshark (Top menu: Capture -> Options).

With wireshark running, enter your VM's IP address along with a user name and a generic password.  Type a few chat messages to make sure everything works.  Once you are satisfied, stop capturing packets in wireshark.

## Packet Analysis
Use the wireshark output to answer the following questions:
1. For each port exposed describe the behavior of packet traffic.  
   * At which packet in an authentication exchange (port 3461) does the client send the user name and password?  
   * What packet contains the server's response?  Are these consistent across login attempts?  
   * Likewise, what does the receive port (3462) look like?  
   * How do both of these exchanges differ from the broadcast port (3463)? 
2. Using figure 19.2 in the book (p. 563) as a template, describe the authentication packet's header (e.g. version, length, service type, etc.).  Include a screenshot of the packet in wireshark in your submission.   