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


### 3. Desktop Icons on NVIDIA Jetson Nano with Ubuntu
Here are the main icons displayed on the Ubuntu desktop of the NVIDIA Jetson Nano:
![1-3 바탕화면](https://github.com/user-attachments/assets/4fb39b2f-8e03-4cf5-a692-05d14a7781d9)
**Chromium Web Browser**: A web browser available by default on Ubuntu, used to browse the internet.

- **NVIDIA Jetson Developer Zone**: A link to NVIDIA Jetson's developer resources. Here, you can find materials, guides, and tutorials related to Jetson Nano.

- **NVIDIA Jetson Zoo**: A collection of pre-trained AI models and libraries available for use on the Jetson Nano. These resources are helpful for deep learning and computer vision projects.

- **NVIDIA Support Forums**: A link to the NVIDIA support forums where Jetson users can ask questions, share information, and solve problems together.

- **L4T README**: Documentation related to NVIDIA's L4T (Linux for Tegra) software. This provides instructions on setting up and using L4T on the Jetson Nano.

- **NVIDIA Jetson Community**: A link to the Jetson user community, where users can interact and share knowledge with other Jetson enthusiasts.

### 4. Installing Korean Input Method on Ubuntu
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


