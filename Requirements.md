# 📄 Smart Inventory System — Requirements Document

## 1. Project Overview
The Smart Inventory System uses a Raspberry Pi and OpenCV to monitor a table and detect when objects are missing, based on a captured "fully stocked" baseline image.

---

## 2. Functional Requirements

| ID   | Requirement Description                                             |
|------|---------------------------------------------------------------------|
| FR1  | System shall capture a baseline image of the full inventory.       |
| FR2  | System shall capture images at regular intervals or on demand.     |
| FR3  | System shall compare the current image to the baseline.            |
| FR4  | System shall detect and flag differences beyond a defined threshold. |
| FR5  | System shall print a message or trigger an alert when an item is missing. |
| FR6  | System shall allow manual resetting of the baseline image.         |

---

## 3. Non-Functional Requirements

| ID    | Requirement Description                                         |
|-------|-----------------------------------------------------------------|
| NFR1  | System must process images in under 2 seconds.                 |
| NFR2  | System must operate autonomously when powered.                |
| NFR3  | System should be usable via command line or button interface. |
| NFR4  | The alert should be noticeable (e.g., LED, buzzer, console message). |

---

## 4. Hardware Components

- Raspberry Pi 4 Model B
- Pi Camera module or USB webcam
- Breadboard (optional for LED/buzzer)
- Jumper wires
- Power supply

---

## 5. Software Stack

- Raspberry Pi OS (Bookworm/Bullseye)
- Python 3
- OpenCV
- NumPy
- (Optional) `gpiozero` / `RPi.GPIO` for hardware alerts
- (Optional) Flask or MQTT for remote access

---

## 6. Initial Milestones

| Day | Task                                               |
|-----|----------------------------------------------------|
| 1   | Set up Raspberry Pi + Camera                      |
| 2   | Capture and save baseline image                   |
| 3   | Capture and compare current image                 |
| 4   | Implement threshold difference detection          |
| 5   | Trigger alert on detected change                  |
| 6+  | Add GUI or hardware indicators (stretch goal)     |
