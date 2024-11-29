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

### **1. Guide to Installing and Using jtop**
![image](https://github.com/user-attachments/assets/d079f666-bbf1-4942-b85b-2fbaf9a67536)

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

### **2.Jetson Nano Cooling Fan Installation Guide**
![image](https://github.com/user-attachments/assets/d5961ef5-b318-42d2-8655-6f0dfadc7c54)
## **1) Why Install a Cooling Fan?**
Jetson Nano may experience performance degradation or system instability due to high temperatures. Installing a cooling fan helps to manage the device's temperature efficiently.

## **2) Required Materials**
1. Cooling fan (PWM-supported, 5V)
2. Screwdriver and attachment tools
3. Jetson Nano device

## **3) How to Install the Cooling Fan**

### (1) *Connect the Cooling Fan*
- Attach the cooling fan's red (+), black (-), and yellow (PWM) cables to the pin headers on the Jetson Nano.
  - Pin configuration: **5V, GND, PWM**
- Refer to the image below for proper connection.

### (2) *Fix the Fan*
- Place the fan on top of the Nano's heatsink and secure it with screws.
- If screws are unavailable, you can use adhesive or double-sided tape.

## **4) Configuring the Cooling Fan**

### *(1)Open the Terminal*
Run the following command in the terminal to control the fan's speed:

```bash
sudo sh -c 'echo 128 > /sys/devices/pwm-fan/target_pwm'
```
- 128 sets the fan speed. (Range: 0–255)
- Adjust the value to set the desired fan speed.
### *(2) Check the Temperature*
- Use the jtop command to monitor the current temperature.
- After the fan operates, the temperature may drop by approximately 10°C.

### **3. USB Camera Setup on Jetson Nano**

## **1) Camera Used**
We used the **Logitech C270 USB Camera**, which is compatible with Jetson Nano and easy to configure.
![image](https://github.com/user-attachments/assets/3717d0dc-7b1d-4a75-a544-f834eaf94ddd)

## **2) Verifying USB Camera Connection**
## *(1) Connect the Camera:*
   - Plug the USB camera into one of the Jetson Nano's USB ports.

## *(2) Check Camera Recognition:*
   Open the terminal and run the following command to check if the camera is recognized:
   ```bash
   ls /dev/vi*
   ```
- Example output:
```bash
crw-rw----+ 1 root video 81, 0 Jan 7 18:29 /dev/video0
```
- If /dev/video0 appears, the camera is recognized successfully.

## **3) Downloading USB Camera Code**
- Clone the GitHub Repository: Use the following command to download the USB Camera setup code from GitHub:
```bash
git clone https://github.com/jetsonhacks/USB-Camera.git
```
- Navigate to the Directory: Move into the downloaded directory:
```bash
cd USB-Camera
```
- Verify Directory Contents: Use the ls command to view the files in the directory.

## **4) Ready to Use**
![image](https://github.com/user-attachments/assets/780daafd-42ff-4eec-acb4-f29e5dce62f7)

### **4.Face Detection with USB Camera on Jetson Nano**

![image](https://github.com/user-attachments/assets/04444234-83e6-489c-b46b-b661ba009a24)

## **1) Prerequisites**
Make sure you have followed the steps to set up the USB camera as described in the previous sections.

## **2) Navigate to the USB Camera Directory**
Navigate to the directory where the USB camera scripts were cloned:

```bash
cd USB-Camera
```
List the files in the directory to verify the presence of the face detection script:
```bash
ls
```
You should see the following files:
- face-detect-usb.py
- usb-camera-gst.py
- usb-camera-simple.py
  
## **3) Run the Face Detection Script**
To perform face detection using the USB camera, execute the following command:
```bash
python3 face-detect-usb.py
```

# **Day 3**
1. Introduction
This report summarizes the project conducted as part of the microdegree coursework, focusing on implementing a real-time hand gesture recognition system using NVIDIA Jetson Nano. The primary objective was to utilize machine learning for classifying hand gestures (e.g., thumbs up, thumbs down) using a camera.

2. Background
Classification Overview: Classification is the process of grouping entities based on shared attributes or characteristics. In this project, images captured by a camera were classified into predefined categories (e.g., "thumbs up" and "thumbs down") using a deep learning model.

![image](https://github.com/user-attachments/assets/b9f001af-fcfa-4369-a707-4d738d2b915d)

3. Project Details
3.1. Jetson Nano Setup
- Device: NVIDIA Jetson Nano
- Mode of Operation: Headless mode (no monitor connected)
- Camera Used: Raspberry Pi Camera Module V2.x
- Software Framework: PyTorch for training and deploying the neural network
- Environment: No internet connection was required for the setup.

3.2. Camera Configuration
1. Camera Selection:
- CSI Camera (e.g., Raspberry Pi Camera Module V2): 
 from jetcam.csi_camera import CSICamera
camera = CSICamera(width=224, height=224, capture_device=0)
 - This camera was chosen for its compatibility and reliability with Jetson Nano.
 - 
Alternative (USB Camera):
 - USB cameras such as the Logitech C270 were considered as an alternative

2. Camera Initialization:
 - The camera was activated with the following commands:
camera.running = True
print("camera created")

 - Successful initialization was verified when the output displayed:
  camera created
![image](https://github.com/user-attachments/assets/cfa90366-f84b-4a0c-b7a1-6e37470022b8)
3.3. Implementation
Steps:

1. Data Collection:
- Images of gestures such as "thumbs up" and "thumbs down" were collected using the camera.
2.Model Training:
- A deep learning model was trained on Jetson Nano to classify the collected images into the appropriate categories.

 ![image](https://github.com/user-attachments/assets/6c2369e0-f57c-4018-a9f3-27bdf1b9d7ae)
3. Real-Time Prediction:
- After training, the model was deployed to perform live predictions.
- Example outcomes:
 - A "thumbs up" gesture was correctly classified as "thumbs up."
 - A "thumbs down" gesture was correctly classified as "thumbs down."
![image](https://github.com/user-attachments/assets/6c2369e0-f57c-4018-a9f3-27bdf1b9d7ae)
![image](https://github.com/user-attachments/assets/cbb78c29-2229-4006-a6cb-44c8f3213d3d)

4. Observations
1. The system effectively captured images and processed real-time predictions.
2. The gesture recognition was accurate, with clear differentiation between "thumbs up" and "thumbs down."
3. During testing, a "System throttled due to Over-current" warning was observed, suggesting the need for improved power management or cooling solutions.

5. Conclusion
This project successfully demonstrated the capability of NVIDIA Jetson Nano to handle real-time computer vision tasks using a simple camera setup. The implementation highlighted the potential for using affordable, compact devices for machine learning applications.

# **DAY 4**
:  Reading Sensor Signals with Jetson Nano
Objective : 
The focus of today's session was to integrate Arduino with Jetson Nano to read and process signals from a Grove dust sensor. This included setting up the development environment for Arduino, performing basic functionality tests with the Blink program, and implementing code to measure dust concentration.

1. Arduino Installation
To enable Arduino development:

1. Downloaded the Arduino package from the official website.
(2) Updated the Linux package manager using
(3) Installed Arduino software:
(4) Verified the installation by launching Arduino:
 
2. Arduino Basic Test: Blink
- Tested the Arduino setup using the Blink example, which toggles an LED on and off every second.
- Successfully confirmed Arduino's functionality with the following code:
![image](https://github.com/user-attachments/assets/789f8b37-ca81-401c-a8bf-0523de1b6ddf)
![image](https://github.com/user-attachments/assets/f821d253-40f1-4626-b1fa-7ef5de36cd68)
![image](https://github.com/user-attachments/assets/a5f88aa1-71d4-4dae-9458-64147a8f10d2)
-> Arduino connected with the Grove dust sensor and powered via USB. 

3. Dust Sensor Integration
Sensor Details:
- Sensor used: Grove dust sensor
- Connection: Connected to pin 8 on the Arduino board.
Implementation:
The code below was implemented to measure dust concentration in ug/m3 (micrograms per cubic meter) over 30-second intervals:
![image](https://github.com/user-attachments/assets/692aa760-2766-4cb0-b29f-7fa3458a86f1)
-> Full setup with the sensor connected to the Arduino.

![image](https://github.com/user-attachments/assets/e6e20b0b-a6da-4fd4-9308-11a521dbf278)
 # Dust Sensor Integration
#### **Dust Sensor Code Implementation**
The following code is a program that uses the Grove Dust Sensor to measure dust concentration in real-time. The sensor calculates the concentration based on the duration of LOW signals, and the results are output in units of μg/m³.

```cpp
int pin = 8;
unsigned long duration;
unsigned long starttime;
unsigned long sampletime_ms = 30000;  // 30초 동안 샘플링
unsigned long lowpulseoccupancy = 0;
float ratio = 0;
float concentration = 0;

void setup()
{
    Serial.begin(9600);  // 시리얼 통신 시작
    pinMode(pin, INPUT); // 센서를 INPUT 모드로 설정
    starttime = millis(); // 시작 시간 초기화
    Serial.println("미세먼지 측정을 시작합니다...");
    Serial.println("==============================");
}

void loop()
{
    duration = pulseIn(pin, LOW); // LOW 신호 지속시간 측정
    lowpulseoccupancy += duration;

    if ((millis() - starttime) > sampletime_ms) // 30초 간격으로 계산
    {
        ratio = lowpulseoccupancy / (sampletime_ms * 10.0); // LOW 신호 비율 계산
        concentration = 1.1 * pow(ratio, 3) - 3.8 * pow(ratio, 2) + 520 * ratio + 0.62; // 농도 계산 (ug/m³)

        Serial.println("==============================");
        Serial.print("미세먼지 농도: ");
        Serial.print(concentration);
        Serial.println(" ug/m³");

        // 대기질 상태 표시
        Serial.print("대기질 상태: ");
        if (concentration <= 30) {
            Serial.println("좋음");
        } else if (concentration <= 80) {
            Serial.println("보통");
        } else if (concentration <= 150) {
            Serial.println("나쁨");
        } else {
            Serial.println("매우 나쁨");
        }

        Serial.println("------------------------------");
        lowpulseoccupancy = 0; // 초기화
        starttime = millis(); // 시간 초기화
    }
}

4. Observations
(1) The Arduino board successfully communicated with the Grove dust sensor, providing real-time dust concentration data.
(2) Using the 30-second interval sampling, the sensor outputs consistent and accurate readings.
(3 The results were displayed in the Arduino serial monitor for further analysis.
(4) Conversion equations from the sensor datasheet were implemented to convert the pulse duration to dust concentration.
 Arduino basic, blink 활용
![image](https://github.com/user-attachments/assets/a9e3edca-6082-4833-891e-8f986d8512e1


