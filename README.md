# Face Recognition Door Lock System with Wi-Fi Module for Smart Home System

This project implements a **face recognition-based door lock system** using a Wi-Fi module. The system uses facial recognition to identify authorized users and unlock the door. The system is developed using **C** and **C++**.

Demo of the Smart Home Video Project: https://www.youtube.com/watch?v=SxPO22OO0eE&t=0s 
## Features

- **Face Recognition**: Identifies users based on their facial features and can save more than one face.
- **Wi-Fi Integration**: Uses an ESP8266/ESP32 Wi-Fi module for remote control and communication.
- **Secure Door Locking**: Automatically unlocks the door when an authorized face is recognized.
- **Real-Time Feedback**: Displays status updates for successful or failed recognition.

## Components Used

- **Microcontroller**: STM32F411RE, ESP32.
- **Camera Module**: Used for capturing images for face recognition ( ESP32 CAM ).
- **Wi-Fi Module**: ESP8266/ESP32 for internet communication.
- **Servo Motor**: Used to control the door lock mechanism.
- **Face Recognition Software**: OpenCV.

## Getting Started

### Prerequisites

Before running this system, ensure you have the following installed:

- **Arduino IDE** (or any other compatible IDE)
- **OpenCV** (for face recognition if you're using a PC for processing)
- **ESP8266/ESP32 Libraries** (for communication between the microcontroller and Wi-Fi module)
- **12V door lock or Servo Motor** (for Unlocking the door lock)

### Hardware Setup

1. **Microcontroller**: Connect the ESP32 or Arduino to your computer via USB.
2. **Camera Module**: Connect the camera module to the appropriate pins on the microcontroller.
3. **Servo Motor**: Wire the servo motor to the microcontroller to control the lock.
4. **Wi-Fi Module**: If using ESP8266, connect it to the microcontroller for Wi-Fi access.

### Software Setup

1. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/Alansi775/ESP32-CAM_Face_Recognition_Door_Lock.git
    cd ESP32-CAM_Face_Recognition_Door_Lock
    ```

2. Open the **Arduino IDE** and load the code from the `src` folder onto your microcontroller.

3. Install the necessary libraries:
   - **ESP32/ESP8266 Libraries** for communication.
   - **OpenCV** (if you're using a PC for face recognition).
   - **Servo Motor Library** for controlling the locking mechanism.

4. Update the Wi-Fi credentials in the code (`wifi_config.h`) with your **SSID** and **Password**.

5. Train the facial recognition model (if applicable) to ensure it correctly recognizes faces.

6. Upload the code to your microcontroller.

### Running the System

1. Power on the system. The Wi-Fi module should connect to the configured network.
2. The camera module will start capturing images and attempt to recognize faces.
3. If an authorized face is detected, the servo motor will unlock the door.
4. If an unauthorized face is detected, the system will notify you and deny access.

## File Structure

```plaintext
/src
    ├── main.cpp           # Main program for controlling the system
    ├── wifi_config.h      # Wi-Fi configuration settings
    └── face_recognition.cpp  # Face recognition logic
/include
    └── face_recognition.h # Header file for face recognition functions
/libs
    └── OpenCV            # Library for face recognition (if using on PC)
