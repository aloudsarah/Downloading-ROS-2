# Downloading ROS 2
This repository explains how to download ROS in Windows

## Stages
- Enabling WSL2
- Downloading Ubuntu
- Installing ROS 2
- Environment Setup

## 1. Enabling WSL2
#### **First Step: Open PowerShell**
  1. Press the **Start** button (or Windows key)
  2. Type **PowerShell**
  3. Right click on **Windows PowerShell**
  4. Choose **Run as administrator**
  5. Click **Yes** to allow the app to make changes.


#### **Second Step: Install WSL**
Type the following command in PowerShell:
 ```bash
wsl --install
```

## 2. Downloading Ubuntu
After installing WSL, run the following command to install Ubuntu 22.04 LTS (recommended for ROS 2 Humble):
  ```bash
wsl --install -d Ubuntu-22.04
```

**Important**: *Once the installation finishes*, **restart** your computer.

## 3. Installing ROS 2
After restarting, open your Ubuntu terminal from the **Start** menu and set up your username/password
then run the following commands sequentially:

 #### Step 1: Set up locale & system updates

 ```bash
sudo apt update && sudo apt upgrade -y
```
```bash
sudo apt install software-properties-common curl -y
```
#### Step 2: Add the ROS 2 repository keys
```bash
sudo curl -sSL [https://raw.githubusercontent.com/ros/rosdistro/master/ros.key](https://raw.githubusercontent.com/ros/rosdistro/master/ros.key) -o /usr/share/keyrings/ros-archive-keyring.gpg
```
```bash
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] [http://packages.ros.org/ros2/ubuntu](http://packages.ros.org/ros2/ubuntu) jammy main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
```
#### Step 3: Install ROS 2 Humble Desktop
```bash
sudo apt update
```
```bash
sudo apt install ros-humble-desktop -y
```
## 4. Environment Setup
To automatically source ROS 2 every time you open a new terminal, run:

```bash
echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
```
``` bash
source ~/.bashrc
```
## Verify Installation
Check that ROS 2 is properly loaded:
``` bash
echo $ROS_DISTRO
```
Expected output: ```humble```
