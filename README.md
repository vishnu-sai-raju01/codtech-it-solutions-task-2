 Home Automation System

A simple and efficient Home Automation System using Arduino that allows users to control home appliances like lights, fans, and more via Bluetooth and voice commands.

---

## 📌 Features

- Control appliances using smartphone (via Bluetooth)
- Supports voice command integration
- Uses relay modules for switching high voltage devices
- Low-cost and beginner-friendly
- Expandable and customizable

---

## 🛠️ Components Used

| Component            | Quantity |
|----------------------|----------|
| Arduino Uno          | 1        |
| HC-05 Bluetooth Module | 1      |
| 4-Channel Relay Module | 1      |
| Jumper Wires         | As needed |
| Smartphone with Bluetooth | 1   |
| Power Supply (5V)    | 1        |
| Light Bulb / Fan     | 1+       |

---

## ⚙️ How It Works

1. The Arduino receives commands from a smartphone via Bluetooth.
2. It then activates or deactivates connected devices through relay modules.
3. Commands can be manual (buttons in app) or voice-based.
4. Voice commands are processed through a mobile app and sent over Bluetooth.

---

## 🔌 Circuit Connections

| Arduino Pin | HC-05 Module | Relay IN | Function       |
|-------------|--------------|----------|----------------|
| TX (D1)     | RX           | -        | Send to Bluetooth |
| RX (D0)     | TX           | -        | Receive from Bluetooth |
| D7          | -            | IN1      | Control Device 1 |
| D6          | -            | IN2      | Control Device 2 |
| GND         | GND          | GND      | Ground          |
| 5V          | VCC          | VCC      | Power Supply    |

> **⚠️ Note**: Use a voltage divider for Arduino TX to HC-05 RX to avoid over-voltage.

---

## 📲 Mobile App

- Use any Bluetooth terminal app (e.g., **Bluetooth Terminal**, **Arduino Bluetooth Controller**, or custom MIT App Inventor app).
- Send commands like:
  - `A` → Turn ON Light
  - `B` → Turn OFF Light
  - `C` → Turn ON Fan
  - `D` → Turn OFF Fan

You can customize command mappings in code.

---

## 🧾 Example Arduino Code

```cpp
char data = 0;

void setup() {
  pinMode(7, OUTPUT); // Light
  pinMode(6, OUTPUT); // Fan
  Serial.begin(9600);
}

void loop() {
  if (Serial.available()) {
    data = Serial.read();
    if (data == 'A') digitalWrite(7, HIGH);
    else if (data == 'B') digitalWrite(7, LOW);
    else if (data == 'C') digitalWrite(6, HIGH);
    else if (data == 'D') digitalWrite(6, LOW);
  }
}
