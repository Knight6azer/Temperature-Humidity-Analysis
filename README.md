# Temperature & Humidity Data Collection and Analysis

[![Status: Archived](https://img.shields.io/badge/Status-Archived-lightgrey.svg)]()
[![Hardware: Arduino](https://img.shields.io/badge/Hardware-Arduino-00979D.svg)](https://www.arduino.cc/)
[![Language: Python](https://img.shields.io/badge/Language-Python-3776AB.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

> ⚠️ **Repository Status: Archived**  
> This is a foundational academic tutorial project (Jan 2025) demonstrating microcontroller serial communication, real-time data acquisition, CSV persistence, and statistical scatter visualization via pandas and matplotlib. It is preserved for reference.

---

## 📌 Features

- **Microcontroller Interfacing**: Reads live temperature and humidity metrics from an Arduino Uno over serial USB.
- **Data Filtering & Cleaning**: Validates ranges to discard physical sensor noise and malformed transmission strings.
- **CSV Data Persistence**: Stores normalized environmental records into structured CSV formats for exploratory analysis.
- **Statistical Analytics & Visualization**: Generates summary statistics via pandas and renders temperature vs. humidity scatter plots.

---

## 🛠️ Prerequisites

### Hardware
- Arduino Uno / Nano with DHT11 or DHT22 temperature & humidity sensor
- USB connecting cable

### Software
- Python 3.9+
- Arduino IDE

---

## 🚀 Setup & Execution

### 1. Environment Installation
```bash
# Clone the repository
git clone https://github.com/Knight6azer/Temperature-Humidity-Analysis.git
cd Temperature-Humidity-Analysis

# Create and activate virtual environment
python -m venv venv
# Windows:
venv\Scripts\activate
# Linux/macOS:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### 2. Arduino Firmware Setup
Upload your DHT sensor sketch to the Arduino to output serial telemetry at 9600 baud in the following format:
```
Temperature: 28.5	Humidity: 65.0
```

### 3. Run Data Acquisition
Edit the COM port in `code.py` to match your system (e.g. `'COM3'` on Windows or `'/dev/ttyACM0'` on Linux):
```bash
python code.py
```

The script will gather data, output summary statistics, write to `temperature_humidity_data.csv`, and render the visualization plot.

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
