## Circuit Diagram

The hardware prototype is built around an ESP32 development board and integrates two HC-SR04 ultrasonic sensors, an LCD1602 display and an active buzzer.

The circuit was designed and verified using Wokwi before implementation on the physical prototype.

<img width="974" height="719" alt="9ab51da02599cb34b799b7b84a9ff23b" src="https://github.com/user-attachments/assets/9076bd33-88db-42c6-ab86-fc8f29e3e3c4" />


## System Architecture

The following diagram illustrates the functional architecture and data flow of the system.

                 Moving Object
                       │
        ┌──────────────┴──────────────┐
        ▼                             ▼
   HC-SR04 Sensor 1             HC-SR04 Sensor 2
        │                             │
        └──────────────┬──────────────┘
                       ▼
                     ESP32
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
   Speed Calculation  LCD1602     Buzzer Alarm
      & Filtering     Display
