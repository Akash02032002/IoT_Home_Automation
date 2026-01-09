# ESP32 Firebase IoT Home Automation Project with Web Dashboard

## IoT Home Automation using ESP32 Firebase Realtime Database with Web Dashboard and manual relay control via switches or buttons.

### Project Overview
This project enables you to:

Control 4 electrical appliances using relays (active-low).
Monitor and update relay status using Firebase Realtime Database.
Use a web dashboard (hosted on GitHub Pages) to control relays from anywhere in the world.
Add manual control using either push buttons or latched switches.
Get real-time feedback and sync between the web dashboard and the physical ESP32 board.

### How the ESP32 Firebase IoT Home Automation Project works
How the ESP32 Firebase Project Works
ESP32 connects to your Wi-Fi router and authenticates with Firebase using the provided credentials.
On startup, all relays are initialized to OFF (HIGH for active-low relays).
A web dashboard, deployed on GitHub Pages, updates Firebase when a user toggles a relay switch.
ESP32 constantly listens for Firebase RTDB updates and changes the relay state accordingly.

Manual control via physical buttons is handled using the AceButton library:
Latched switch: Relay stays ON while the switch is pressed and OFF when released.
Push button: Relay toggles ON/OFF on every release event.
The current state is written back to the Firebase Realtime Database to keep the system in sync.
Manual control the ESP32 Relays

### Required Components:
ESP32 DevKIT V1 Amazon
4-channel 5V SPDT Relay Module Amazon
Latched switches or Push buttons