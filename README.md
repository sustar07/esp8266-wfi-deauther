Wi-Fi Deauther with ESP32/ESP8266
This project uses an ESP32 or ESP8266 to perform Wi-Fi deauthentication attacks by sending deauth packets to targeted devices, causing them to disconnect from their Wi-Fi network temporarily. It is intended for educational purposes and security testing only.

Features
Sends deauthentication packets to disconnect devices from a Wi-Fi network.
Web-based interface to control the deauther.
Can target specific devices or disrupt entire networks.
Lightweight and portable using ESP32/ESP8266.
Components Required
ESP32 or ESP8266 board (e.g., NodeMCU, Wemos D1 Mini)
Micro USB Cable
Computer (for flashing firmware)
External battery (optional for portable usage)
Installation and Setup
1. Install Arduino IDE and ESP Board Support
Download and install Arduino IDE.
In Arduino, go to File -> Preferences, and add the following URL to the Additional Board Manager URLs:
bash
Copy code
https://arduino.esp8266.com/stable/package_esp8266com_index.json
or for ESP32:
arduino
Copy code
https://dl.espressif.com/dl/package_esp32_index.json
Go to Tools -> Board -> Boards Manager and install the ESP8266 or ESP32 board package.
2. Install Required Libraries
Install the following libraries via Arduino Library Manager (Sketch -> Include Library -> Manage Libraries...):

ESP8266WiFi or WiFi.h for ESP32
WiFiClient
DNSServer
ESPAsyncWebServer
3. Flashing the Firmware
Clone or download the Wi-Fi Deauther code from the GitHub repository for ESP8266 or the relevant repository for ESP32.
Open the project in Arduino IDE.
Select your ESP8266/ESP32 board model from Tools -> Board.
Select the correct COM port under Tools -> Port.
Upload the code to your ESP8266/ESP32 by clicking the upload button in the Arduino IDE.
4. Access the Deauther Web Interface
Once the code is uploaded and the ESP is powered on:

The ESP8266/ESP32 will create a Wi-Fi network named pwned or similar.
Connect to this network using a smartphone, tablet, or computer.
Open a browser and go to the IP address 192.168.4.1 to access the web interface.
Usage
1. Scanning for Networks
From the web interface, scan for available Wi-Fi networks and devices.
The interface will display a list of networks and the devices connected to them.
2. Deauthentication Attack
Select a network to target or individual clients connected to the network.
Click "Deauth" to begin sending deauthentication packets.
Devices connected to the targeted network will be disconnected.
3. Attack Modes
Deauth Attack: Disconnects devices by sending deauthentication packets.
Beacon Flood Attack: Floods the area with fake access points.
Probe Request Attack: Broadcasts probe requests to confuse Wi-Fi clients.
Customization
Target Specific Devices: You can configure the interface to target only specific devices connected to the network by selecting their MAC addresses.
Adjust Packet Rate: You can modify the packet send rate for different performance and effectiveness results.
Portable Setup: Connect the ESP8266/ESP32 to a portable battery for on-the-go testing.
Legal Disclaimer
This project is for educational purposes and should only be used in environments where you have explicit permission to test network security. Unauthorized use of this tool to disrupt Wi-Fi networks is illegal and unethical. Use responsibly.

References
ESP8266 Deauther by Spacehuhn
ESP32 Board by Espressif
Arduino IDE
