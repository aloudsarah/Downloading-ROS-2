# Downloading-ROS
this repository explains how to download ROS on ubuntu 
## Stages
- Enabling WSL2
- Downloading Ubuntu
- Downloading ROS2

## Enabling WSL2
- First Step: Open PowerShell
  1- Press the Start button (Windows icon in the corner)
  2- Type PowerShell
  3- Right click on "Windows PowerShell"
  4- Choose "Run as administrator"
  5- ########

- Second Step: Installing WSL
  type this command in your powershell, this will install WSL
 ```bash
wsl --install
```
  then type this command, this will install Ubuntu 22.04, make sure it is 22.04 otherwise ROS unbable to work
  ```bash
wsl --install -d Ubuntu-22.04
```
after being downloading successfully, **restart** your device

