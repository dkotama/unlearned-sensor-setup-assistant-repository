---

# Smart Environmental Sensor OUTTX-110 Datasheet

---

## Key Specifications
- **Measurements**: Temperature, humidity, and atmospheric pressure
- **Comfort Index**: Real-time calculation and output
- **Dual Communication Protocols**: UART (CSV format) and HTTP POST (JSON format)
- **Wi-Fi Connectivity**: 2.4 GHz, 802.11 b/g/n
- **Operating Conditions**: -40°C to +80°C, 0 to 100% RH, 300–1100 hPa
- **Power Consumption**: ~152 mA (active), ~60 µA (sleep)
- **Dimensions**: ~100 × 80 mm (breadboard size)
- **Use Cases**: Home automation, weather stations, greenhouses, smart offices, health monitoring

---

## General Description
- The Smart Environmental Sensor OUTTX-110 is a compact, IoT-enabled device designed for environmental monitoring. It measures **temperature**, **humidity**, and **atmospheric pressure**, and computes a **Comfort Index** to assess environmental quality.
- Dual data output options: **UART** for local integration (e.g., Raspberry Pi) and **HTTP POST** for cloud or server integration. A built-in web server allows configuration of the target server IP, enhancing ease of use.
- Features low-power operation, Wi-Fi connectivity, and a modular design for smart homes, weather stations, industrial monitoring, and more.
- Unique strengths: **real-time Comfort Index calculation**, dual communication protocols, and user-friendly configuration.

---

## Manufacturer Information
- **Manufacturer**: Distributed System Lab, Okayama University
- **Address**: 3-1-1 Tsushima-naka, Kita-ku, Okayama 700-8530, Japan
- **Website**: [Okayama University](https://www.okayama-u.ac.jp/)
- **Production Date**: Prototype Batch 2025-01 (June 2025)
- **Product Code**: SES-OUTTX-110-2025
- **Contact**: Email university administration for inquiries (support available via the research portal)
- **Support**: Technical support available within 48 hours for prototype-related inquiries

---

## Performance
- **Temperature**: 
  - Range: -40 to +80°C
  - Accuracy: ±0.5°C
  - Resolution: 0.1°C
- **Humidity**: 
  - Range: 0–100% RH (non-condensing)
  - Accuracy: ±2% RH
  - Resolution: 0.1% RH
- **Pressure**: 
  - Range: 300–1100 hPa
  - Accuracy: ±0.12 hPa
  - Resolution: 0.03 hPa
- **Comfort Index**:
  - Range: 0 to 100
  - Response Time: ~2 seconds
  - Formula:  
    ```
    100 - (|temp - 22| * 2 + |humidity - 50| * 1.5 + |pressure - 1013| * 0.05)
    ```

---

## Electrical
- **Power Supply**: 2.2V to 3.6V (3.3V nominal)
- **Control Voltage**: 3.3V logic
- **Output Type**: Digital (UART and HTTP POST)
- **Interface**: UART, Wi-Fi (2.4 GHz, 802.11 b/g/n)
- **Data Output**:
  - **Format**:  
    - UART: CSV format  
      Example:  
      ```
      Temp: 25.5°C, Humidity: 60.2%, Pressure: 1013.25 hPa, Comfort Index: 85.0
      ```
    - HTTP POST: JSON payload
      Example:  
      ```
      {"temp":25.5,"humidity":60.2,"pressure":1013.25,"comfort_index":85.0}
      ```
- **Power Consumption**:
  - Active: ~152 mA
  - Sleep/Idle: ~60 µA
  - Communication Active: ~162 mA

---

## Mechanical
- **Dimensions**:
  - Sensor Module: ~25 × 15 mm
  - Overall (breadboard): ~100 × 80 mm
- **Weight**: ~50 g
- **Materials**: PCB core with optional plastic or metal enclosures
- **Mounting**: Breadboard-based prototype design

---

## Environmental
- **Operating Temperature**: -40 to +80°C
- **Storage Temperature**: -50 to +100°C
- **Humidity**: 0 to 100% RH (non-condensing)
- **Pressure**: 300 to 1100 hPa
- **Environmental Ratings**: Prototype only (no additional ruggedization stated)

---

## Extra Information
- **Compliance**:
  - Placeholder for anticipated RoHS, CE, FCC compliance (to be verified with the manufacturer).
- **Troubleshooting Guide**:
  - **No UART output**:
    - Check power and connections.
    - Ensure UART parameters match (115200 baud rate).
  - **No HTTP POST**:
    - Verify Wi-Fi connection and target server IP.
  - **Erratic readings**:
    - Secure wiring and reduce noise interference.
- **Calibration**:
  - Recalibration recommended every 6–12 months at standard conditions (22°C, 50% RH, 1013 hPa).
  - Adjust offsets via firmware (contact the manufacturer for assistance).

---

**Ambiguities/Concerns Detected**:
1. **Contact Information Ambiguity**: The datasheet mentions "Email university administration for lab inquiries," but there is no direct lab email or phone number provided.
2. **Compliance Placeholder**: RoHS, CE, FCC compliance is only anticipated but not officially certified as stated in the datasheet.
3. **Mechanical Materials**: The description of materials is vague and does not confirm whether a plastic/metal enclosure is included by default.
