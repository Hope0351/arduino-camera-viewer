Arduino Camera Viewer
  
A robust and user-friendly Arduino-based project that leverages the ESP32-CAM module to capture and stream live video or still images over a Wi-Fi network. This project enables real-time camera viewing through a web browser, making it ideal for applications such as home surveillance, remote monitoring, or DIY camera projects.
Table of Contents

Features
Hardware Requirements
Software Requirements
Installation
Usage
Configuration
Troubleshooting
Contributing
License
Acknowledgments
Contact

Features

Live Video Streaming: Stream camera footage in real-time via a web interface.
Image Capture: Capture high-quality still images and save them to a MicroSD card (optional).
Wi-Fi Connectivity: Access the camera feed from any device on the same network.
Customizable Settings: Adjust resolution, frame rate, and other camera parameters.
Lightweight and Portable: Built for the compact and affordable ESP32-CAM module.
Open Source: Fully customizable and extensible for advanced use cases.

Hardware Requirements
To build and run this project, you will need:

ESP32-CAM Module: Equipped with an OV2640 camera (2MP resolution).
MicroSD Card: Optional, for storing captured images (4GB or larger recommended).
USB-to-Serial Adapter: For programming the ESP32-CAM (e.g., FTDI programmer).
Power Supply: 5V via USB or external power source.
Jumper Wires: For connecting the ESP32-CAM to the programmer.
Computer: For uploading code via the Arduino IDE.

Software Requirements

Arduino IDE: Version 2.0 or later (download here).
ESP32 Board Support Package: Add via Arduino IDE Boards Manager (instructions here).
Libraries:
esp_camera: For camera functionality (included with ESP32 board package).
WiFi: For network connectivity (included with ESP32 board package).


Web Browser: For accessing the camera feed (e.g., Chrome, Firefox).

Installation
Follow these steps to set up the Arduino Camera Viewer:

Install the Arduino IDE:

Download and install the Arduino IDE from the official website.
Add ESP32 board support by following the ESP32 Arduino setup guide.


Clone or Download the Repository:

Clone this repository:git clone https://github.com/Hope0351/arduino-camera-viewer.git


Alternatively, download the ZIP file and extract it.


Connect the ESP32-CAM:

Wire the ESP32-CAM to an FTDI programmer or USB-to-serial adapter:
GND → GND
5V → VCC
TX → RX (FTDI)
RX → TX (FTDI)
GPIO 0 → GND (for programming mode)


Insert a MicroSD card if using image storage.


Open the Project:

Open the arduino-camera-viewer.ino file in the Arduino IDE.
Ensure the correct board (AI-Thinker ESP32-CAM) and port are selected in the IDE.


Install Dependencies:

The required esp_camera and WiFi libraries are bundled with the ESP32 board package. Verify they are installed via the Arduino IDE Library Manager.


Upload the Code:

Click the "Upload" button in the Arduino IDE.
Disconnect GPIO 0 from GND after uploading to run the program.



Usage

Power the ESP32-CAM:

Connect the ESP32-CAM to a 5V power source or USB.
Open the Serial Monitor in the Arduino IDE (set to 115200 baud) to view the boot log.


Connect to Wi-Fi:

The ESP32-CAM will connect to the configured Wi-Fi network and display its IP address in the Serial Monitor (e.g., 192.168.x.x).


Access the Camera Feed:

On a device connected to the same Wi-Fi network, open a web browser.
Navigate to http://<ESP32-CAM-IP-ADDRESS> (replace with the IP shown in the Serial Monitor).
Use the web interface to view the live stream or capture images.


Optional Image Storage:

If a MicroSD card is installed, images can be saved by triggering the capture function (configured in the web interface or code).



Configuration
To customize the project, modify the following in arduino-camera-viewer.ino:

Wi-Fi Credentials:const char* ssid = "YOUR_WIFI_SSID";
const char* password = "YOUR_WIFI_PASSWORD";


Camera Settings:
Adjust resolution (e.g., FRAMESIZE_UXGA for 1600x1200) in the camera_config structure.
Modify frame rate or quality as needed.


Web Server Port:
Default is port 80. Change server.begin(80) if a different port is required.



Troubleshooting

No IP Address in Serial Monitor:
Verify Wi-Fi credentials are correct.
Ensure the ESP32-CAM is within Wi-Fi range.
Check the Serial Monitor baud rate (115200).


Camera Feed Not Displaying:
Confirm the OV2640 camera is properly connected and functional.
Ensure the browser is accessing the correct IP address.
Try a different browser or device.


Upload Errors:
Verify GPIO 0 is connected to GND during upload.
Check that the correct board and port are selected in the Arduino IDE.


MicroSD Card Issues:
Ensure the card is formatted as FAT32 and properly inserted.



For additional help, check the Issues section or open a new issue.
Contributing
We welcome contributions to enhance the Arduino Camera Viewer! To contribute:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Make your changes and commit (git commit -m "Add your feature").
Push to your branch (git push origin feature/your-feature).
Open a pull request.

Please ensure your code follows the project’s coding style and includes appropriate documentation.
License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgments

ESP32 Arduino Core for providing the foundation for ESP32-CAM development.
The Arduino community for extensive resources and tutorials.
Random Nerd Tutorials for inspiration and example projects.

Contact
For questions, suggestions, or issues, please:

Open an issue on this repository.
Contact the maintainer at hope0351@outlook.com.
Follow updates on Twitter: @Hope0351.

Happy streaming!
