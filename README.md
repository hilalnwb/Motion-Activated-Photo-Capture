# Motion-Activated Photo Capture

### Objective
This project demonstrates the development of a motion-activated photo capture system using a PIR sensor, ESP32 microcontroller, and supporting components. The system detects motion, captures an image, and stores it on a microSD card, ensuring efficient and cost-effective real-time monitoring.

### Components Used
- **BC547 Transistor**
- **ESP32-CAM**
- **MicroSD Card**
- **PIR Motion Sensor**
- **FTDI Programmer**
- **Jumper Wires**
- **5V Power Supply**

### Software Used
- **KiCad EDA**
- **Arduino IDE**

### Background
The PIR sensor is responsible for detecting motion within its range and signaling the ESP32 microcontroller to capture an image. The BC547 transistor acts as a switch, enabling the PIR sensor to interface with the ESP32 and indirectly manage higher power components. Captured images are stored on a microSD card, with an optional feature to transmit the data via Wi-Fi to a mobile device or cloud storage. The Arduino IDE was used to write and upload the code, initializing the PIR sensor, triggering image capture, and managing data storage or transmission. This low-cost solution ensures real-time monitoring and provides an efficient and affordable security documentation system.

<div align="center">
  <img src="https://github.com/user-attachments/assets/7b6441de-075e-412e-91ad-3b13d04bc61f" alt="Background Diagram" width="600">
</div>

### Circuit Schematic (KiCad Schematic Editor)

<div align="center">
  <img src="https://github.com/user-attachments/assets/860d463f-cf4e-4700-bd2c-9aa121c658bc" alt="Circuit Schematic" width="600">
</div>

### Prototyping & Testing Phase
The prototyping phase began with uploading the code to the ESP32-CAM and connecting its 5V and GND pins to the breadboard's power and ground rails. The PIR sensor's output was connected to the base of the BC547 transistor through a 1kΩ resistor, while the emitter was grounded, and the collector was linked to an LED via a 220Ω resistor. A 10kΩ pull-up resistor was added between +5V and the collector to stabilize the circuit. The GPIO pin IO14 was then connected to the transistor's base through the resistor, allowing signal input. This setup enabled the system to detect motion and respond by activating the ESP32-CAM for image capture.

<div align="center">
  <img src="https://github.com/user-attachments/assets/af83b1aa-1010-44a2-bd8e-58ed4acab57d" alt="Prototyping Setup" width="600">
</div>

### PCB Designing (KiCad PCB Editor)
The PCB design process started with creating the circuit schematic in KiCad. Components, including the ESP32-CAM, PIR sensor, transistor, resistors, and LED, were placed strategically to minimize wiring complexity and ensure optimal functionality. Connections were routed with appropriate trace widths for power and signal lines, while maintaining clearances to avoid short circuits. The design was thoroughly checked using the Design Rule Check (DRC) tool to ensure accuracy and reliability. Labels and annotations, including the authors' names, were added to the design for clarity and attribution.

<div align="center">
  <img src="https://github.com/user-attachments/assets/a5183086-1224-4d3c-b088-5e0b67630801" alt="Updated PCB Design" width="600">
</div>

### 3D Model & Final Render

<div align="center">
  <img src="https://github.com/user-attachments/assets/86950424-adbb-41d0-86b8-b66144a62261" alt="3D Model" width="600">
</div>

### Printed Diagram

<div align="center">
  <img src="https://github.com/user-attachments/assets/84d7eced-49d9-443c-b53b-8adccf245254" alt="Printed Diagram" width="600">
</div>

### Chemical PCB Etching
The PCB was fabricated using the chemical etching method. The design was printed onto a transparency film with a laser printer and transferred to a copper-clad board using heat from an electric iron. The board was then submerged in a ferric chloride solution, which dissolved unwanted copper, leaving only the required circuit traces. After the etching process, holes were drilled for component leads, and the board was cleaned to remove any residues. The cleaned PCB was then prepared for soldering the components.

<div align="center">
  <img src="https://github.com/user-attachments/assets/be0dfef8-e35b-416c-9681-a276a7fb8777" alt="PCB Etching" width="600">
</div>

### Home Stretch
To enhance the system's maintainability, female header pins were used for the ESP32-CAM, BC547 transistor, and PIR motion sensor, allowing easy replacement of components if needed. The header pins were carefully soldered onto the PCB, ensuring proper alignment with the traces. Special attention was given to the positioning of the transistor's base, emitter, and collector pins to ensure functionality. The ESP32-CAM module was securely connected, with careful handling of power, ground, and GPIO pins to avoid errors.

<div align="center">
  <img src="https://github.com/user-attachments/assets/f270df24-b06a-4b10-9161-6aa794457e32" alt="Final Assembly" width="600">
</div>

### Final Testing
To test the system, we used a small airplane-shaped keychain as the object to trigger motion detection. The keychain, made of lightweight metal and painted in vibrant colors, provided a clear and distinct target for the PIR sensor. Its compact size and reflective surface made it an ideal choice to demonstrate the system's sensitivity and precision in detecting motion.

<div align="center">
  <img src="https://github.com/user-attachments/assets/b21f1c8a-3404-48c4-8530-7bc7b19da741" alt="Keychain" width="600">
</div>

Upon detecting the keychain's movement, the PIR sensor activated the ESP32-CAM, which promptly captured an image. The captured image was stored on the microSD card, showcasing the seamless integration of motion detection, image capture, and storage functionalities. This test confirmed that the system performed as expected, validating its ability to detect motion and document events in real time.

<div align="center">
  <img src="https://github.com/user-attachments/assets/f4031966-40d8-4804-b43c-1e37efc089a2" alt="Captured Image" width="600">
</div>

### Conclusion
The Motion-Activated Photo Capture project was a resounding success. The system effectively captured images upon motion detection, thanks to the ESP32-CAM, PIR sensor, microSD card, and BC547 transistor. The transistor played a crucial role as a switch, enabling the low-power PIR sensor to communicate with the ESP32 microcontroller. Through this project, we gained valuable experience in circuit design, PCB fabrication, and troubleshooting, culminating in the creation of a functional and affordable security system.

### Thanks!
[Random Nerd Tutorials](https://randomnerdtutorials.com/esp32-cam-pir-motion-detector-photo-capture/)
