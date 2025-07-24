HOME AUTOMATION SYSTEM

A simple and efficient Home Automation System using Arduino that allows users to control home appliances like lights, fans, etc., via Bluetooth and voice commands.

FEATURES:

• Control appliances via smartphone using Bluetooth
• Supports voice command integration
• Uses relay modules to control high-voltage devices
• Low-cost and beginner-friendly
• Easily expandable and customizable for future needs

COMPONENTS USED:

• Arduino Uno – 1
• HC-05 Bluetooth Module – 1
• 4-Channel Relay Module – 1
• Jumper Wires – As required
• Smartphone with Bluetooth – 1
• 5V Power Supply – 1
• Appliances (Bulb, Fan, etc.) – 1 or more

HOW IT WORKS:

• The HC-05 Bluetooth module receives commands from a smartphone
• Arduino interprets the command and activates/deactivates the relays
• The relays switch connected appliances ON or OFF
• Optional voice commands can be used through the smartphone app

CIRCUIT CONNECTIONS:

• Arduino TX (D1) → HC-05 RX
• Arduino RX (D0) → HC-05 TX
• Arduino D7 → Relay IN1 (Device 1)
• Arduino D6 → Relay IN2 (Device 2)
• GND → Common Ground
• 5V → VCC (Power supply for HC-05 and relay module)

Note: Use a voltage divider between Arduino TX and HC-05 RX to avoid over-voltage.

MOBILE APP COMMANDS:
Use any Bluetooth terminal app or custom MIT App Inventor app. Send the following commands:

• ‘A’ → Turn ON Light
• ‘B’ → Turn OFF Light
• ‘C’ → Turn ON Fan
• ‘D’ → Turn OFF Fan

FOLDER STRUCTURE:
 
 HomeAutomation/
 ArduinoCode/ → home_automation.ino
 App/ → MIT_App_Inventor.app  
 Circuit_Diagram/ → home_automation_circuit.png
 README.txt

FUTURE IMPROVEMENTS:

• Add Wi-Fi control using ESP32
• Integrate with Google Assistant or Alexa
• Add sensors to monitor temperature, motion, etc.
• Display appliance status on LCD or smartphone
• Add security features like password or fingerprint access

