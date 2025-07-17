#  LED Control Using Push Button | Arduino Project 🔴

![Status](https://img.shields.io/badge/status-in_progress-blue)
![Arduino](https://img.shields.io/badge/Platform-Arduino-green)
![TinkerCad](https://img.shields.io/badge/Simulated_on-TinkerCad-orange)
![Level](https://img.shields.io/badge/Difficulty-Beginner-lightgrey)

This beginner-friendly Arduino project demonstrates how to control an LED using a push button. It introduces fundamental concepts of digital input/output and simple delay-based timing.

---

##  Project Description :

When the button is pressed, the Arduino turns ON an LED for a defined period (1 second), then turns it OFF. This is a great entry-level project for learning how to work with buttons, LEDs, and control logic using Arduino.

---

##  Components Used :

| Component          | Quantity |
|--------------------|----------|
| Arduino UNO        | 1        |
| LED (any color)    | 1        |
| 220Ω Resistor      | 1        |
| Push Button        | 1        |
| Breadboard         | 1        |
| Jumper Wires       | As needed |
| USB Cable          | 1        |

---

## 🔌 Circuit Connections

- **LED:**
  - Anode (+) → Digital Pin **13** (via 220Ω resistor)
  - Cathode (−) → GND
- **Push Button:**
  - One pin → Digital Pin **2**
  - Other pin → GND

> Make sure to connect the button properly across the breadboard centerline, and consider using an internal pull-down resistor or debounce logic for better stability.

---

##  Arduino Code Explanation :

```cpp
// 🔧 Define pin numbers
int ledPin = 13;
int buttonPin = 2;
int buttonState = 0;

void setup() {
  // 🛠️ Set pin modes
  pinMode(ledPin, OUTPUT);
  pinMode(buttonPin, INPUT);
}

void loop() {
  // 📥 Read the button state
  buttonState = digitalRead(buttonPin);

  // ⚡ If button is pressed, turn LED ON
  if (buttonState == HIGH) {
    digitalWrite(ledPin, HIGH);
    delay(1000); // 🕒 LED stays ON for 1 second
  } 
  else {
    // 💡 Otherwise, turn LED OFF
    digitalWrite(ledPin, LOW);
  }
}
