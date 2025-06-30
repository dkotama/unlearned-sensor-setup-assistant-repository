# OULTX125R - Dual-Light Sensor System

## Key Specifications
- Dual-light sensor system for ambient and directional light measurement.
- ESP32 DevKitC-based microcontroller for reliable data acquisition.
- Compact form factor with low power consumption.
- Output via GPIO13 (digital HIGH/LOW) and USB Type-C UART Serial interface.
- CE, FCC, and RoHS compliant.

---

## General Description
The OULTX125R is an advanced dual-light sensor system designed for precision environmental sensing in modern IoT deployments. It measures both ambient light levels and directional light intensity, making it suitable for applications like home automation, energy management, and security systems. Leveraging an ESP32 DevKitC microcontroller, the device provides reliable data acquisition. Additional features include a standardized digital output on GPIO13 and three distinct LED indicators for real-time operational feedback. Its compact design and energy-efficient operation make it ideal for constrained environmental monitoring projects.

---

## Manufacturer Information
- Part Number: OULTX125R
- Manufacturer: **No specific company name provided in the document.**
- For additional details on bulk orders or configurations, users are advised to contact their sales representative.

---

## Performance
- **Resolution**: 12-bit ADC with a range of 0 to 4095 digital values.
- **Accuracy (post-calibration)**: ±5%.
- **Sampling Rate**: 1 Hz (configurable).
- **Latency**: Less than 50 milliseconds.
- **Response Time**: Under 10 milliseconds, ideal for detecting rapid changes in light levels.

---

## Electrical
- **Power Supply**:
  - Operating Voltage: 3.3V DC or 5V DC.
  - Power Consumption: <500mW.
  - Primary Power: Via USB Type-C, requiring a minimum of 500mA.
  - Alternative Power: 5V DC through ESP32's VIN pin (minimum 500mA current recommended).
- **Control Voltage**: No information provided.
- **Output Type**:
  - Digital: GPIO13 outputs 3.3V HIGH or 0V LOW.
  - Analog: Sensor data is output as raw analog (0-3.3V), converted to 12-bit digital values ranging from 0-4095.
- **Interface Options**:
  - GPIO13: For integration with microcontrollers (e.g., Raspberry Pi, Arduino).
  - UART Serial Interface: USB Type-C connection for debugging and monitoring at 115200 baud rate.
- **Data Output**:
  - Format: 
    ```
    Ambient: <value> | Directional: <value> | Diff: <value> | Output Pin 13: <HIGH/LOW>
    ```
  - Example:
    ```
    Ambient: 1500 | Directional: 3500 | Diff: 2000 | Output Pin 13: HIGH
    Ambient: 2000 | Directional: 1950 | Diff: 50 | Output Pin 13: LOW
    ```

---

## Mechanical
- **Dimensions**:
  - ESP32 DevKitC Module: ~50mm (L) x 25mm (W).
  - Dual-light sensor module: 20mm x 15mm.
- **Weight**: ~25 grams (including LEDs).
- **Mounting Options**: No information provided.
- **Materials**: No information provided.

---

## Environmental
- **Operating Temperature**: -20°C to +60°C.
- **Storage Temperature**: No information provided.
- **Environmental Ratings**: IP20 (suitable for indoor use, dust protected but not water-resistant).
- **Vibration Resistance**: No information provided.
- **Humidity**: Operates within 10% to 90% relative humidity (non-condensing).

---

## Extra Information
- **Certifications**:
  - CE and FCC certified (ESP32 module).
  - RoHS compliant (manufactured without hazardous substances).
- **Troubleshooting Guide**:
  - **No Serial Output on Raspberry Pi**:
    - Verify UART connection and device recognition (`ls /dev/tty*`).
    - Set script baud rate to 115200 and ensure proper power connection.
  - **Sensor Saturation (Constant 4095)**:
    - Adjust sensitivity or test under different lighting conditions.
  - **LEDs Not Lighting Up**:
    - Confirm wiring to GPIO pins and use a 220Ω resistor on the cathode.
    - Ensure light levels exceed activation thresholds.
  - **No GPIO13 Output**:
    - Check connections and ensure light difference exceeds 100 to signal HIGH.
  - **Unstable Readings**:
    - Secure connections, mitigate electrical noise, and perform calibration in stable lighting environments.
