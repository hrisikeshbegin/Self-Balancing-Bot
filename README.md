
# 2-Wheel Self-Balancing Robot

A self-balancing robot built using **Arduino**, **MPU6050 gyroscope/accelerometer**, and an **L298N motor driver**.  
The robot uses sensor fusion and a PID control loop with a software Kalman filter to maintain its balance on two wheels.



## Features
- Real-time angle measurement using **MPU6050 (I2C)**
- **PID control algorithm** for stable balancing
- Controlled via **Arduino Uno/Nano**
- Motor control through **L298N H-Bridge driver**
- Compact 2-wheel chassis design



## Components Used
- Arduino Uno / Nano  
- MPU6050 (Gyroscope + Accelerometer)  
- L298N Motor Driver  
- DC Geared Motors (x2)  
- Wheels (x2)  
- Li-ion / LiPo Battery Pack  
- Robot chassis (custom/DIY)  
- Jumper wires & connectors  



## Circuit Diagram
- **MPU6050 → Arduino**  
  - VCC → 5V  
  - GND → GND  
  - SDA → A4  
  - SCL → A5  

- **L298N → Arduino**  
  - IN1 → D8  
  - IN2 → D9  
  - IN3 → D10  
  - IN4 → D11  
  - ENA/ENB → PWM pins (D5, D6)  

- **Power**  
  - Motors powered via external battery to L298N  
  - Arduino powered via USB or regulated supply  



## Working Principle
1. The **MPU6050** measures tilt angle (pitch).  
2. Data is filtered using **complementary filter / Kalman filter** for stability.  
3. A **PID controller** calculates correction signals.  
4. The **L298N driver** adjusts motor speed and direction to maintain balance.  



## Installation & Setup
1. Clone this repository:  
   ```bash
   git clone https://github.com/hrisikeshbegin/Self-Balancing-Bot.git
2.   Open the project in **Arduino IDE**.
    
3.  Select the correct **Board** (Arduino Uno/Nano) and COM **Port**.
    
4. Click **Upload** to flash the code to your Arduino.


Developed With Love By Hrisikesh Kashyap along with Other Members of the Robotics Club N.E.R.D.S.
