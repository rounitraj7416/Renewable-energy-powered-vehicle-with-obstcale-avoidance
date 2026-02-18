# Renewable-energy-powered-vehicle-with-obstcale-avoidance
# 🤖 Arduino Obstacle Avoiding Robot

An autonomous robot project that navigates its environment using an ultrasonic sensor to detect obstacles. If the path is blocked, the robot stops, scans left and right using a servo-mounted sensor, and turns toward the clearer path.

## 🚀 Features

- **Autonomous Navigation:** Moves forward by default and reacts to obstacles.
- **Smart Scanning:** Uses a servo motor to "look" left and right when blocked.
- **Decision Logic:** Compares distances on both sides to choose the best direction.
- **L298N Integration:** Controls two DC motors with full directional support.

## 🛠️ Hardware Requirements

- **Microcontroller:** Arduino Uno (or compatible board)
- **Motor Driver:** L298N H-Bridge Module
- **Sensor:** HC-SR04 Ultrasonic Sensor
- **Servo:** SG90 Micro Servo (or similar)
- **Motors:** 2x DC Gear Motors + Wheels + Chassis
- **Power:** Battery pack (e.g., 2x 18650 Li-ion or 9V)

## 🔌 Wiring & Pin Connections

### L298N Motor Driver
| Arduino Pin | Component Pin | Function |
| :--- | :--- | :--- |
| **7** | IN1 | Left Motor Forward |
| **6** | IN2 | Left Motor Backward |
| **5** | IN3 | Right Motor Forward |
| **4** | IN4 | Right Motor Backward |

### Sensors & Servo
| Arduino Pin | Component | Function |
| :--- | :--- | :--- |
| **A1** | HC-SR04 Trig | Ultrasonic Trigger |
| **A2** | HC-SR04 Echo | Ultrasonic Echo |
| **10** | Servo Signal | Rotates Sensor |

> **Note:** Ensure the L298N GND and Arduino GND are connected together.

## 📦 Software Dependencies

You will need the following libraries installed in your Arduino IDE:

1.  **Servo.h** (Standard built-in library)
2.  **NewPing.h** (Must be installed)
    - *To install:* Go to **Sketch** -> **Include Library** -> **Manage Libraries**, search for `NewPing` by Tim Eckel, and install it.

## ⚙️ Configuration

You can tweak the following variables at the top of the `.ino` file to fit your robot's chassis and environment:

- `maximum_distance`: Maximum range for the sensor (default: 200cm).
- `distancelimit`: Threshold for obstacle detection (default logic checks `< 45`).
- **Servo Angles:** - Center: `115`
  - Right Look: `50`
  - Left Look: `170`

## 🚀 How to Run

1.  Assemble the hardware according to the wiring table.
2.  Open the `.ino` file in the Arduino IDE.
3.  Install the `NewPing` library.
4.  Connect your Arduino via USB and select the correct Board/Port.
5.  Click **Upload**.
6.  Place the robot on the floor and power it on!

## 📄 License

This project is open for personal use and modification.
