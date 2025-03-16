# EEE428_Instrumentation
 
# Factory Alcohol Detection System

This project implements a **Factory Alcohol Detection System** designed to prevent intoxicated employees from entering the workplace. The system integrates alcohol detection technology with access control, ensuring compliance with workplace safety regulations.

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [System Components](#system-components)
4. [Repository Structure](#repository-structure)
5. [Installation and Setup](#installation-and-setup)
6. [Usage](#usage)
7. [Documentation](#documentation)
8. [Contributing](#contributing)
9. [License](#license)

---

## Project Overview

The Factory Alcohol Detection System is a safety mechanism designed to:
- Detect alcohol levels in employees' breath using an MQ-3 alcohol sensor.
- Verify employee identity using a fingerprint reader (FPM10A).
- Control access to the factory using electrically operated gates.
- Log incidents (e.g., access denied due to high alcohol levels) for compliance and reporting.

The system ensures compliance with the **Occupational Safety and Health Act, 2001 (No. 9 of 2001) of Eswatini** and other workplace safety standards.

---

## Features

- **Alcohol Detection**: Accurately measures breath alcohol concentration (BrAC) using the MQ-3 sensor.
- **Access Control**: Grants or denies access based on alcohol levels and employee identity.
- **Incident Logging**: Logs all access attempts and incidents to an SD card for compliance.
- **Alarm System**: Triggers visual and auditory alarms for access violations.
- **User-Friendly Interface**: Simple and intuitive for employees to use.

---

## System Components

### Hardware
- **Microcontroller**: Arduino Uno R3.
- **Alcohol Sensor**: MQ-3 gas sensor.
- **Fingerprint Reader**: FPM10A module.
- **Gate Mechanism**: 24V DC electric door locks.
- **Alarm System**: 85 dB buzzer and LED indicators.
- **Power Supply**: 24V DC with overcurrent and overvoltage protection.
- **Data Storage**: SD card module.

### Software
- **Arduino IDE**: For programming the microcontroller.
- **Libraries**:
  - `SoftwareSerial.h`: For serial communication with the fingerprint reader.
  - `SD.h`: For interfacing with the SD card module.
  - `FPM.h`: For interfacing with the FPM10A fingerprint reader.

---

## Repository Structure

```
Factory-Alcohol-Detection-System/
│
├── base/
│   ├── packages.tex       % LaTeX packages for the report
│   └── style.tex          % Custom styles for the report
│
├── images/                % Images and diagrams
│   ├── circuit_diagram.png
│   ├── mantrap_drawing.png
│   ├── assembly.png
│   └── flowChart.png
│
├── sections/              % LaTeX sections for the report
│   ├── 00_abstract.tex
│   ├── 00_front_page.tex
│   ├── 01_introduction.tex
│   └── appendix.tex
│
├── bibliography.bib       % Bibliography for the report
├── report.tex             % Main LaTeX document
└── README.md              % Project overview and documentation
```

---

## Installation and Setup

### Hardware Setup
1. **Connect Components**:
   - Connect the MQ-3 alcohol sensor, FPM10A fingerprint reader, and SD card module to the Arduino Uno as per the circuit diagram (`images/circuit_diagram.png`).
   - Connect the 24V DC electric door locks and alarm system to the appropriate output pins.

2. **Power Supply**:
   - Ensure the power supply provides a stable 24V DC output with overcurrent and overvoltage protection.

### Software Setup
1. **Install Arduino IDE**:
   - Download and install the [Arduino IDE](https://www.arduino.cc/en/software).

2. **Upload Code**:
   - Open the `Alcohol_Detection_System.ino` file in the Arduino IDE.
   - Upload the code to the Arduino Uno.

3. **Install Libraries**:
   - Install the required libraries (`SoftwareSerial.h`, `SD.h`, `FPM.h`) via the Arduino Library Manager.

---

## Usage

1. **Employee Entry**:
   - Employees approach the mantrap and scan their fingerprint.
   - The system verifies their identity and prompts them to provide a breath sample.

2. **Alcohol Detection**:
   - The MQ-3 sensor analyzes the breath sample.
   - If the alcohol level is within limits, the gate opens, and access is granted.
   - If the alcohol level exceeds the limit, the alarm triggers, and access is denied.

3. **Incident Logging**:
   - All access attempts and incidents are logged to the SD card for compliance and reporting.

---

## Documentation

The project documentation is available in the `report.tex` file. It includes:
- System overview and design.
- Schematics and electrical drawings.
- Mechanical drawings.
- Source code and implementation details.

To compile the report:
1. Install a LaTeX distribution (e.g., [TeX Live](https://www.tug.org/texlive/)).
2. Compile the report using:
   ```bash
   pdflatex report.tex
   bibtex report
   pdflatex report.tex
   pdflatex report.tex
   ```

---

## Contributing

Contributions to this project are welcome! To contribute:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Submit a pull request with a detailed description of your changes.

---

