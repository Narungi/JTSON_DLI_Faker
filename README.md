# JTSON_DLI_Faker

# **Day 1**

### **1. NVIDIA Jetson Nano Developer Kit**

![잭슨](https://github.com/user-attachments/assets/7b49c6a7-f222-4f06-922c-1d3ed24d0889)

1. **Heatsink**: The heatsink is used to cool down the processor of the Jetson Nano. It helps dissipate heat during extended usage, preventing overheating.

2. **GPIO Pins (General Purpose Input/Output)**: These pins allow you to connect various external devices, such as sensors, LEDs, and switches, for control and interaction.

3. **Micro-USB Port**: This port is used to provide power or transfer data. It's commonly used to power the board.

4. **Ethernet Port**: This port is for wired internet connection, allowing the board to connect to a network for data exchange.

5. **USB 3.0 Ports**: High-speed USB ports for fast data transfer. You can connect USB devices like a mouse, keyboard, or external hard drive.

6. **USB 2.0 Port**: A standard USB port for connecting USB devices. It’s slower than USB 3.0 but is widely compatible.

7. **HDMI Port**: Used to connect to a monitor or TV. It supports video and audio output.

8. **DC Power Jack**: A jack for supplying power to the board. Usually, a 5V 4A power adapter is used to ensure stable power.

9. **Camera Connector**: This port is for connecting a MIPI CSI camera module. It’s commonly used in vision projects that utilize Jetson Nano’s AI capabilities.


### **2. Ubuntu Installation**
Here are the steps to install **Ubuntu** on the NVIDIA Jetson Nano. Ubuntu is a popular Linux-based operating system, often used for AI, machine learning, and other development projects.

![1-2 우분투 설치](https://github.com/user-attachments/assets/b26f2ce9-48db-4ff3-84da-b66e4b96bac2)

1. **Basic System Setup**: During the initial setup, you’ll select essential settings, including anguage, time zone, and keyboard layout to personalize your system.

2. **Installing Essential Software**: The installation process will automatically add necessary drivers and software packages required for the Jetson Nano to operate properly.

3. **Network Configuration**: You’ll configure the internet connection, allowing for software updates and downloading additional packages that might be needed for development.

4. **Completing the Installation**: After the setup, the system will finalize the installation and apply the configurations. Once done, you’ll have a fully functional Ubuntu environment on the Jetson Nano.


### **3. Desktop Icons on NVIDIA Jetson Nano with Ubuntu**
Here are the main icons displayed on the Ubuntu desktop of the NVIDIA Jetson Nano:
![1-3 바탕화면](https://github.com/user-attachments/assets/4fb39b2f-8e03-4cf5-a692-05d14a7781d9)
**Chromium Web Browser**: A web browser available by default on Ubuntu, used to browse the internet.

- **NVIDIA Jetson Developer Zone**: A link to NVIDIA Jetson's developer resources. Here, you can find materials, guides, and tutorials related to Jetson Nano.

- **NVIDIA Jetson Zoo**: A collection of pre-trained AI models and libraries available for use on the Jetson Nano. These resources are helpful for deep learning and computer vision projects.

- **NVIDIA Support Forums**: A link to the NVIDIA support forums where Jetson users can ask questions, share information, and solve problems together.

- **L4T README**: Documentation related to NVIDIA's L4T (Linux for Tegra) software. This provides instructions on setting up and using L4T on the Jetson Nano.

- **NVIDIA Jetson Community**: A link to the Jetson user community, where users can interact and share knowledge with other Jetson enthusiasts.

### **4. Installing Korean Input Method on Ubuntu**
![1-4 한글설치](https://github.com/user-attachments/assets/5bbc03e7-b5cb-4524-a108-fe3a8d3143c1)

1. **Install Fcitx Korean Input Method**: Open the terminal and enter the following commands to install the Fcitx Korean input method:
   ```bash
   sudo apt-get update
   sudo apt-get install fcitx-hangul
2. **Change Input Method System** : Go to Settings** > Region & Language, and click on Manage Installed Languages at the bottom. Here, change the Keyboard input method system to Fcitx.

3. **Reboot the System** : Reboot your system to apply the changes.

4. **Configure Fcitx** : After rebooting, a keyboard icon should appear in the upper right corner of the screen. Click it and select*Configure. If the icon is not visible, open Fcitx Configuration from the applications menu.

5. **Add Korean Input Method** : In the Fcitx settings window, go to the Input Method tab, click the '+' button, and select Hangul to add it.

6. **Set Korean/English Switch Key** : In the Global Config tab, click on Trigger Input Method and press the key you want to use for switching between Korean and English (e.g., the Korean/English key).
![1-5 한영키 전환](https://github.com/user-attachments/assets/023052f2-e468-4786-94a6-79785b9ff364)

# **Day 2**
![image](https://github.com/user-attachments/assets/d079f666-bbf1-4942-b85b-2fbaf9a67536)
### **1. Guide to Installing and Using jtop**

## **1) What is jtop?**
`jtop` is a powerful tool for monitoring the system status of NVIDIA Jetson devices in real time. It provides detailed information about the system resources on devices like the Jetson Nano, including:

- **Temperature**: Displays the temperature of key components such as the CPU, GPU, and PMIC (Power Management IC).
- **Resource Usage**:
  - CPU and GPU usage.
  - Memory and swap usage.
  - Power consumption.
- **Process Management**:
  - Lists running processes and their resource usage.
- **Device Information**:
  - Shows hardware and software details, including the JetPack version.

## **2) How to Install jtop**
### *(1) Install Python3-pip*
Before installing `jtop`, you need to install `pip`, the Python package manager. Run the following commands:

```bash
sudo apt update
sudo apt install python3-pip -y
```
During installation, you may see the following message:
```bash
Do you want to continue? [Y/n]
```
Enter Y to proceed.

### *(2) Install jetson-stats*
The jtop tool requires the jetson-stats library. To install the latest version, run:
```bash
sudo -H pip3 install -U jetson-stats
```

### *(3) Verify Installation*
After installation, confirm that jetson-stats is properly installed by checking its version:
```bash
jetson-stats --version
```
Example output:
```bash
jetson-stats-4.2.3
```
### *(4) Troubleshooting*
If any errors occur during installation, update your system and try again:
```bash
sudo apt-get update
sudo apt-get upgrade
```
After updating, reinstall jetson-stats:
```bash
sudo -H pip3 install -U jetson-stats
```
### *(5) Run jtop*
Once installed, you can run jtop using the following command:
```bash
jtop
```






# **Day 3**
#1 What is Classification?
Classification refers to the process of organizing or grouping entities based on their shared attributes or common characteristics. For example, grouping apples into one category and bananas into another.

Jetson Nano Project Overview
The guide introduces a PyTorch-based project where:

A deep neural network is trained on the Jetson Nano.
The trained model classifies images collected using a camera.
Development Environment
The project is run in Headless Mode, meaning no monitor is connected to the Jetson Nano.
A Raspberry Pi Camera v2.x is recommended for capturing data.
No internet connection is required for this setup.
Let me know if you need further clarification or additional details about classification, Jetson Nano, or this specific project.

#2. Camera Configuration in Jetson Nano
(1) Import Required Libraries:

For USB cameras, import the USBCamera module:
python
"from jetcam.usb_camera import USBCamera"

For CSI cameras (e.g., Raspberry Pi Camera Module V2), import the CSICamera module:
python
"from jetcam.csi_camera import CSICamera"

(2) Camera Selection:

If you are using a USB camera (e.g., Logitech C270 webcam):
Uncomment the following line in your code and ensure the capture_device is set correctly:
python
"# camera = USBCamera(width=224, height=224, capture_device=0)"
If you are using a CSI camera (e.g., Raspberry Pi Camera Module V2):
Uncomment the following line instead:
python
"camera = CSICamera(width=224, height=224, capture_device=0)"
(3) Verify Device Configuration:

Confirm the capture_device number (e.g., 0 in this case) corresponds to the device ID recognized by your Jetson Nano.

#3. Camera Initialization Code Summary
(1) Import Camera Libraries:

Import the required modules for camera handling:
python
코드 복사
from jetcam.usb_camera import USBCamera
from jetcam.csi_camera import CSICamera
Select the Camera Type:

For a USB camera (e.g., Logitech C270):
Uncomment this line to initialize the camera:
python
"# camera = USBCamera(width=224, height=224, capture_device=0)"
For a CSI camera (e.g., Raspberry Pi Camera Module V2):
Uncomment this line:
python
camera = CSICamera(width=224, height=224, capture_device=0)
Start the Camera:

Enable the camera by setting its running attribute to True:
python
코드 복사
camera.running = True
Confirmation Output:

Print a message to confirm successful camera initialization:
python
코드 복사
print("camera created")
If successful, the output will display: camera created.
![image](https://github.com/user-attachments/assets/b9f001af-fcfa-4369-a707-4d738d2b915d)

![image](https://github.com/user-attachments/assets/cfa90366-f84b-4a0c-b7a1-6e37470022b8)
![image](https://github.com/user-attachments/assets/6c2369e0-f57c-4018-a9f3-27bdf1b9d7ae)
![image](https://github.com/user-attachments/assets/cbb78c29-2229-4006-a6cb-44c8f3213d3d)



