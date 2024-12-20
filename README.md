### Automatic Toll System  

The **Automatic Toll System** is an Arduino-based project aimed at automating toll gate operations. By leveraging components like an ultrasonic sensor and a servo motor, this system detects vehicles approaching the toll gate and automatically opens or closes the gate without manual intervention. This efficient and user-friendly system demonstrates the practical implementation of automation in traffic management.

#### Components Used  
This project was built using the following components:  
- **Arduino UNO**: The microcontroller that processes sensor data and controls the servo motor.  
- **Ultrasonic Sensor**: Used to detect the presence and distance of approaching vehicles.  
- **Servo Motor**: Operates the toll gate by opening and closing it based on commands from the Arduino.  
- **Breadboard and Jumper Wires**: For circuit connections.  
- **Power Supply**: Powers the system.  

#### Circuit Description  
The circuit connects the ultrasonic sensor and servo motor to the Arduino UNO. The ultrasonic sensor measures the distance of vehicles, and the Arduino sends a signal to the servo motor to either open or close the toll gate. The detailed circuit diagram is included in this repository under the `Circuit` folder.  

#### Working Principle  
1. The ultrasonic sensor continuously monitors for approaching vehicles.  
2. If a vehicle is detected within the set range, the Arduino triggers the servo motor to open the toll gate.  
3. After a brief interval, the gate automatically closes, ensuring continuous traffic flow.  

#### Steps to Build  
1. **Assemble the Circuit**: Use the circuit diagram provided to connect the components correctly.  
2. **Program the Arduino**: Upload the `toll_system.ino` file to the Arduino using the Arduino IDE.  
3. **Test the System**: Power the setup and verify that the toll gate opens when a vehicle is detected and closes afterward.  

#### Results  
The Automatic Toll System successfully automates toll gate operations. Vehicles approaching the gate are detected accurately, and the gate opens and closes smoothly, reducing the need for manual effort and improving efficiency.

#### Repository Contents  
- **Code Folder**: Contains the Arduino code (`toll_system.ino`) that powers the system.  
- **Circuit Folder**: Includes the circuit diagram (`circuit_diagram.png`) to replicate the setup.  
- **Images Folder**: Contains pictures of the assembled circuit and the working model.  
- **README.md**: A detailed description of the project.  

#### Folder Structure  
```
Automatic-Toll-System/
├── Code/
│   └── toll_system.ino
├── Circuit/
│   └── circuit_diagram.png
├── Images/
│   ├── project_setup.jpg
│   └── result_video.mp4 (optional)
└── README.md
```

This repository is designed to provide all the necessary resources and documentation for understanding and recreating the Automatic Toll System. Explore the contents to learn more!
