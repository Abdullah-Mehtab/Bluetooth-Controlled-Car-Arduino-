# Bluetooth Controlled Car (with Arduino)

---

## 📌 Introduction
This project focuses on building a Bluetooth-controlled car using an **Arduino Nano** and an **HC-05 Bluetooth module**. The car can be controlled via a mobile phone application, enabling users to move it forward, backward, left, or right.  

We decided to build this project as an extension of a previous course assignment, where we created a **line-following robot car**. Since we already had half of the required components, we took this opportunity to enhance our skills in **networking using Bluetooth communication with Arduino.**  

---

## 📜 Objectives
- Learn how to interface an **HC-05 Bluetooth module** with an **Arduino Nano**.
- Understand motor control using an **L298N motor driver**.
- Develop a mobile-controlled car using **SriTu Hobby Mobile Software**.
- Gain hands-on experience in **electronics and embedded systems**.

---

## 🛠️ Materials Required

| **Component**        | **Quantity** |
|----------------------|-------------|
| Arduino Nano Board  | 1           |
| HC-05 Bluetooth Module | 1       |
| L298N Motor Driver  | 1           |
| Gear Motors         | 4           |
| Robot Wheels       | 4           |
| Rechargeable Batteries | 1 Set   |
| Jumper Wires (M-M, M-F, F-F) | Several |
| Breadboard         | 1           |

---

## 💻 Software Required
- **Arduino IDE** (for coding and uploading the firmware)
- **SriTu Hobby Mobile Software** (for controlling the car via Bluetooth)

---

## 🔌 Circuit Diagram & Wiring
### **Important Concepts Before Wiring:**
- **Ground (GND) = -ve**  
- **VCC/5V = +ve**  
- **TXD (Transmit) → RXD (Receive)**  
- **RXD (Receive) → TXD (Transmit)**  

### **Connections:**
#### **Arduino Nano to HC-05 Bluetooth Module**
| Arduino Nano | HC-05 |
|-------------|-------|
| VCC         | 5V    |
| GND         | GND   |
| TX          | RXD   |
| RX          | TXD   |

#### **Arduino Nano to L298N Motor Driver**
| Arduino Nano | L298N Motor Driver |
|-------------|--------------------|
| ENA         | D9                 |
| IN1         | D2                 |
| IN2         | D3                 |
| IN3         | D4                 |
| IN4         | D5                 |
| ENB         | D10                |

#### **Power Supply**
- **Battery Pack → Motor Driver (GND & 5V)**
- **Rechargeable Batteries in Series for Continuous Power Supply**

---

## 📝 Step-by-Step Implementation

### **1. Setting up the Hardware**
1. Assemble the car body and attach the **gear motors** and **wheels**.
2. Connect the **L298N motor driver** to the motors and power supply.
3. Connect the **HC-05 Bluetooth module** to the Arduino Nano as per the wiring instructions.
4. Ensure proper wiring connections to avoid **short circuits** or damage.

### **2. Programming the Arduino**
1. Open **Arduino IDE**.
2. Copy and paste the provided source code.
3. Select **Arduino Nano** as the board.
4. Select the appropriate **PORT (e.g., CMP-4)** where the Arduino is connected.
5. **IMPORTANT:** Before uploading the code, **disconnect the TX/RX wires** from the Bluetooth module.
6. Upload the code to the Arduino Nano.
7. Once uploaded, **reconnect the TX/RX wires**.

### **3. Setting up the Mobile App**
1. Open **SriTu Hobby Mobile Software**.
2. Navigate to **Control → Bluetooth Car**.
3. Turn ON the mobile’s **Bluetooth**.
4. Click on **Connect to Device**.
5. Select **HC-05** from the available devices.
6. Once connected, the mobile is now successfully paired with the **Bluetooth Car**.

### **4. Testing the Car**
- Use the on-screen controls in the mobile app to move the car **forward, backward, left, and right**.
- Verify that the motors respond correctly to the commands.

---

## ⚠️ Common Issues & Troubleshooting
| Issue | Possible Cause | Solution |
|-------|--------------|----------|
| Bluetooth module not connecting | Incorrect wiring or baud rate mismatch | Check **TX/RX connections**, reset the HC-05, and ensure the correct **baud rate** is set in the code |
| Motors not responding | Power supply issue | Ensure the **L298N motor driver** is receiving adequate power from the battery |
| Code upload failure | TX/RX wires still connected | **Disconnect TX/RX** before uploading the code |
| Car moves erratically | Loose wiring | Double-check all **connections and soldering points** |

---

## 🚧 Challenges Faced
1. **Hardware Procurement:**  
   - Finding quality components was challenging. We had to balance between **cost and quality** to avoid malfunctioning components.  

2. **Assembly & Wiring Issues:**  
   - Initially, incorrect wiring led to minor **circuit issues**.  
   - If a **higher voltage battery** was used improperly, there was a risk of a **short circuit** or **frying the module**.  

3. **Bluetooth Connection Issues:**  
   - Ensuring **proper pairing and stable communication** with the mobile app took some debugging.

4. **Physical Stability of the Car:**  
   - The car **fell off** the table/bed multiple times, leading to minor reassembly efforts.

---

## 📖 References
- [SriTu Hobby: How to Build a Bluetooth Car](https://srituhobby.com/how-to-build-a-bluetooth-control-car-with-arduino-nano-and-hc-05-module/)
- [YouTube Tutorial](https://youtu.be/sncdnRAta_8?si=KzEdPXokUnWk3WHp)

---

## 🎉 Conclusion
This project was an excellent learning experience in **electronics, Arduino programming, and Bluetooth communication**. Despite facing challenges, we successfully built a working **Bluetooth-controlled car** using the **Arduino Nano and HC-05 module**. This project provided hands-on experience in **networking concepts**, **hardware troubleshooting**, and **embedded systems development**.

🚗💨 **Enjoy your own Bluetooth-controlled car!**
