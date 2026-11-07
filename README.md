# Servo Distance Indicator Using Arduino UNO

## 📌 Project Overview

The **Servo Distance Indicator** is an embedded systems project developed using Arduino UNO, an HC-SR04 Ultrasonic Sensor, and an SG90 Servo Motor. The project measures the distance between the sensor and nearby objects and indicates the measured distance through servo motor rotation.

The HC-SR04 ultrasonic sensor transmits ultrasonic waves and receives the reflected waves from an object. Arduino UNO calculates the distance based on the time taken by the waves to travel and return. Based on the calculated distance, the servo motor changes its angular position.

This project demonstrates the practical implementation of ultrasonic sensor interfacing, distance measurement, embedded programming, and servo motor control.

## 🎯 Objectives

- To measure the distance of nearby objects using an ultrasonic sensor.
- To understand ultrasonic wave transmission and reception.
- To calculate distance using echo pulse duration.
- To control servo motor movement based on the measured distance.
- To understand sensor interfacing and actuator control using Arduino.

## 🛠️ Components Required

| Component | Quantity | Purpose |
|---|---|---|
| Arduino UNO | 1 | Main microcontroller |
| HC-SR04 Ultrasonic Sensor | 1 | Distance measurement |
| SG90 Servo Motor | 1 | Indicates distance through rotation |
| Jumper Wires | As required | Circuit connections |
| Breadboard | 1 | Circuit assembly |
| USB Cable | 1 | Programming and power |

## 🔌 Circuit Connections

### HC-SR04 Ultrasonic Sensor

| HC-SR04 Pin | Arduino UNO Pin |
|---|---|
| VCC | 5V |
| GND | GND |
| TRIG | Digital Pin 9 |
| ECHO | Digital Pin 10 |

### SG90 Servo Motor

| Servo Wire | Arduino UNO Pin |
|---|---|
| Red | 5V |
| Brown/Black | GND |
| Orange/Yellow | Digital Pin 6 |

**Note:** If an external 5V supply is used for the servo motor, connect its GND to Arduino GND.

## ⚙️ Working Principle

The project works through the following steps:

1. **Trigger Signal:** Arduino UNO sends a 10-microsecond HIGH pulse to the TRIG pin of the ultrasonic sensor.

2. **Ultrasonic Wave Transmission:** The HC-SR04 sensor transmits ultrasonic waves towards the object.

3. **Echo Reception:** The waves reflect from the object and return to the sensor. The ECHO pin generates a pulse based on the time taken by the waves to return.

4. **Distance Calculation:** Arduino measures the echo pulse duration and calculates the distance using the speed of sound.

5. **Servo Motor Movement:** Based on the measured distance, Arduino calculates the corresponding servo angle and controls the servo motor position.

## 📐 Distance Calculation Formula

The distance is calculated using:

```text
Distance (cm) = (Echo Duration × 0.034) / 2
```

Where:

- Echo Duration = Time taken by ultrasonic waves to travel and return (microseconds).
- 0.034 = Approximate speed of sound in cm/microsecond.
- Division by 2 accounts for the forward and return journey of the sound waves.

**Example:**

If the echo duration is 1000 microseconds:

```text
Distance = (1000 × 0.034) / 2

Distance = 17 cm
```

## 🔄 Distance and Servo Angle Mapping

The servo motor position changes according to the detected distance.

| Object Distance | Servo Angle |
|---|---|
| 2 cm | 180° |
| 10 cm | Approximately 142° |
| 20 cm | Approximately 94° |
| 30 cm | Approximately 47° |
| 40 cm | 0° |

The distance-to-angle mapping can be modified in the Arduino program.

## 💻 Software Requirements

- Arduino IDE
- Arduino UNO Board Package
- Servo Library

## 🧠 Technologies and Concepts Used

- Arduino UNO
- Embedded C/C++
- HC-SR04 Ultrasonic Sensor
- SG90 Servo Motor
- GPIO Interfacing
- Ultrasonic Distance Measurement
- Time-of-Flight Measurement
- PWM-based Servo Control
- Sensor and Actuator Interfacing

## 🔍 Program Logic

1. Initialize the ultrasonic sensor pins.
2. Attach the servo motor to digital pin 6.
3. Generate a trigger pulse.
4. Read the echo pulse duration.
5. Calculate the distance.
6. Convert the measured distance into a servo angle.
7. Move the servo motor to the calculated position.
8. Repeat the process continuously.

## 📂 Project Structure

```text
Servo-Distance-Indicator-Arduino/
│
├── README.md
│
├── Code/
│   └── servo_distance_indicator.ino
│
├── Circuit/
│   └── circuit_diagram.png
│
└── Images/
    ├── project_setup.jpg
    └── working_model.jpg
```

## 🌍 Applications

- Obstacle detection systems
- Robotics and automation
- Distance-based indication systems
- Smart parking assistance prototypes
- Object proximity monitoring
- Educational embedded systems projects

## ⭐ Advantages

- Simple and cost-effective implementation.
- Non-contact distance measurement.
- Real-time distance-based servo positioning.
- Easy integration with Arduino UNO.
- Helps understand sensor and actuator interfacing.

## 🚀 Future Enhancements

- Integrate an LCD display to show the measured distance.
- Add a buzzer for proximity alerts.
- Implement multiple distance thresholds.
- Develop a rotating ultrasonic scanning system.
- Integrate wireless communication for remote monitoring.

## 📚 Learning Outcomes

Through this project, I gained practical experience in:

- Interfacing an HC-SR04 ultrasonic sensor with Arduino UNO.
- Understanding ultrasonic distance measurement.
- Working with digital input and output pins.
- Calculating distance using echo pulse duration.
- Controlling servo motor position using pulse-width-based control.
- Understanding PWM-based servo control.
- Integrating sensors and actuators in an embedded system.

## 📝 Conclusion

The Servo Distance Indicator demonstrates how an ultrasonic sensor and servo motor can work together to create a distance-based indication system. Arduino UNO processes the sensor data and controls the servo motor according to the measured distance.

This project helped develop practical knowledge of embedded systems, sensor interfacing, distance measurement, and actuator control.

---

## 👩‍💻 Project Information

**Project Name:** Servo Distance Indicator

**Domain:** Embedded Systems

**Microcontroller:** Arduino UNO (ATmega328P)

**Programming Language:** Embedded C/C++

**Sensor:** HC-SR04 Ultrasonic Sensor

**Actuator:** SG90 Servo Motor

**Platform:** Arduino IDE

---

**Developed as an Embedded Systems Project.**
