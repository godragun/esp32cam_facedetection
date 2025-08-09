# esp32cam_facedetection

## Overview

This project demonstrates facial detection using the ESP32-CAM microcontroller. The ESP32-CAM is a low-cost, small-size camera module with an ESP32-S chip, widely used for IoT and computer vision applications.

## Features

- Real-time face detection using the ESP32-CAM module
- Live video streaming over Wi-Fi
- Web-based interface for monitoring the camera feed
- Configurable settings for camera resolution and detection sensitivity
- Lightweight and suitable for embedded applications

## Hardware Requirements

- ESP32-CAM module
- FTDI programmer (for flashing the firmware)
- Jumper wires and breadboard (optional)
- 5V power supply

## Software Requirements

- Arduino IDE or PlatformIO
- ESP32 board support installed in Arduino IDE
- Required libraries:
  - `ESP32`
  - `ESPAsyncWebServer`
  - `ESPAsyncTCP`
- Web browser for accessing the camera stream

## Getting Started

### 1. Wiring

Connect the ESP32-CAM to your FTDI programmer as follows:

| ESP32-CAM Pin | FTDI Programmer Pin |
| ------------- | ------------------ |
| 3.3V          | 3.3V               |
| GND           | GND                |
| U0R           | TX                 |
| U0T           | RX                 |
| GPIO0         | GND (for flashing) |

### 2. Flashing the Firmware

1. Download or clone this repository.
2. Open the project in Arduino IDE or PlatformIO.
3. Select the correct board and port in your IDE.
4. Upload the firmware to the ESP32-CAM.
5. Remove GPIO0 from GND and press the reset button to run the program.

### 3. Accessing the Camera Feed

1. Connect the ESP32-CAM to your Wi-Fi network (configure credentials in the source code).
2. After booting, the ESP32-CAM will print its IP address to the serial monitor.
3. Open a web browser and enter the IP address to access the camera interface.

## Face Detection

The firmware includes built-in face detection capabilities using the ESP32's onboard resources. You can view detected faces outlined on the video stream via the web interface.

## Customization

- Adjust camera settings (resolution, brightness) in the source code.
- Modify detection parameters to improve accuracy or speed.
- Integrate with IoT platforms for remote monitoring.

## Troubleshooting

- Ensure you use a stable 5V power supply.
- If the camera does not stream, check your Wi-Fi credentials and serial monitor output.
- For flashing issues, verify the correct wiring and board selection.

## License

This project is licensed under the MIT License.

## Acknowledgements

- [Espressif Systems](https://www.espressif.com/) for the ESP32 platform
- [Arduino ESP32](https://github.com/espressif/arduino-esp32) for board support
- Open-source computer vision libraries and contributors
