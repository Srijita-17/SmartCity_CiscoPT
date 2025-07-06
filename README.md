# SmartCity_CiscoPT 🚦🏙️

**Smart City Simulation using Cisco Packet Tracer 9.0 with Automation (IoT)**  
Developed by: **Srijita Bandyopadhyay**   
Submitted for: **L&T EduTech – Industrial IoT Project**

---

## 📌 Project Description

This project presents a simulation of a Smart City using Cisco Packet Tracer 9.0, incorporating IoT devices for automation in 5 major zones. Each zone operates through sensors, wireless gateways, switches, and programmable JavaScript logic.

Automation is implemented manually and through JavaScript, due to the absence of Blockly support in version 9.0.

---

## 🏙️ Smart City Zones Overview

| Zone | Name            | Description |
|------|-----------------|-------------|
| 1️⃣  | Smart Home (Residential) | Controls fan, lights, door, motion & window detector |
| 2️⃣  | Smart Office           | Automates door & light via motion & smoke sensors |
| 3️⃣  | Smart Traffic Zone     | Uses motion detectors, LEDs & surveillance webcams |
| 4️⃣  | Smart Park             | Automated sprinkler, street lighting via motion |
| 5️⃣  | Emergency System       | Siren, smoke detector, webcam, water drain logic |

---

## ⚙️ Components Used

- Cisco Home Gateway
- 2960 Switches
- PCs & Laptops
- Smart Door, Fan, Lights
- Motion, Smoke, Water Level Sensors
- Webcam, Smart LEDs, Sprinklers, Siren, Drain
- Programming in **JavaScript (IoT)**

---

## 📽️ Execution Video

📺 [Click here to watch the Smart City Demo Video](https://github.com/Srijita-17/SmartCity_CiscoPT/blob/main/SmartCity_ProjectDemoVideo.mp4 )


---

## 📸 Screenshot of Smart City Circuit

![Smart City Logical View](https://github.com/Srijita-17/SmartCity_CiscoPT/blob/main/SimulatedCircuit_SmartCity_Srijita.png)



---

## 🧠 Architecture Summary

All zones are connected via individual switches and gateways. Devices communicate using local IP schemes and share a common SSID (`SmartCity`) with WPA2 security. PCs simulate admin/operator systems.

Sensor events trigger automated device responses via JavaScript logic in the "Programming" tab.

---

## ✍️ Automation Sample (JavaScript)

```javascript
var door = getDevice("SmartDoor_Home");
var light = getDevice("SmartLight_Home");
var fan = getDevice("SmartFan_Home");

function onMotionDetected() {
    door.open();
    light.setPower(true);
    fan.setPower(true);
}

