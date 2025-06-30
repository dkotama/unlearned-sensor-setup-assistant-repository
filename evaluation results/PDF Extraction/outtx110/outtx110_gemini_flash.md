## Key Specifications

- Measures temperature (-40 to +80°C), humidity (0–100% RH), and pressure (300–1100 hPa)
- Computes real-time Comfort Index (0–100)
- Dual output: UART (115200 baud, CSV) and HTTP POST (JSON)
- Built-in web server for configuring target server IP
- Low-power operation with sleep mode (~60 µA)
- Wi-Fi connectivity for IoT applications
- Robust design for long-term stability
- Compact, breadboard-based prototype
- Customizable thresholds for alerts and automation
- High signal integrity for reliable data transmission

## General Description

- The Smart Environmental Sensor OUTTX-110 is a compact, IoT-enabled device that measures temperature, humidity, and atmospheric pressure, computing a Comfort Index to assess environmental quality. It supports dual data output: UART for local integration (e.g., Raspberry Pi) and HTTP POST for cloud/server integration. A built-in web server allows configuration of the target server IP, enhancing IoT flexibility.  The OUTTX-110 combines advanced sensing technologies with onboard processing for accurate, real-time data. Its modular prototype design supports customization, making it ideal for smart homes, weather stations, and industrial monitoring. With low-power operation, Wi-Fi connectivity, and a user-friendly web interface, it’s a versatile solution for modern IoT ecosystems. Key advantages include integrated Comfort Index calculation, dual communication protocols, and ease of configuration, catering to researchers, developers, and end-users.

## Manufacturer Information

- Company Name: Distributed System Lab, Okayama University
- Contact Details:
  - Address: 3-1-1 Tsushima-naka, Kita-ku, Okayama 700-8530, Japan
  - Website: https://www.okayama-u.ac.jp/ (Contact for lab-specific page)
  - Email: Email university administration for lab inquiries; support available via research portal
- Product Identification:
  - Product Code: SES-OUTTX-110-2025
  - Production Date: Prototype Batch 2025-01, June 2025

## Performance

- Speed: Response Time: ~2 seconds
- Accuracy:
  - Temperature: ±0.5°C
  - Humidity: ±2% RH
  - Pressure: ±0.12 hPa
- Precision:
  - Temperature Resolution: 0.1°C
  - Humidity Resolution: 0.1% RH
  - Pressure Resolution: 0.03 hPa
- Response Time: ~2 seconds

## Electrical

- Power Supply: 2.2V to 3.6V (3.3V typical)
- Control Voltage: 3.3V for UART and internal interfaces
- Output Type: UART (CSV), HTTP POST (JSON)
- Interface: Wi-Fi (2.4 GHz, 802.11 b/g/n), UART
- Data Output:
  - Format:
    - UART: CSV (temp,humidity,pressure,comfort_index)
    - HTTP POST: JSON ({"temp":float,"humidity":float,"pressure":float,"comfort_index":float})
  - Example:
    ```
    UART Example: 25.5,60.2,1013.25,85.0
    HTTP POST Example: {"temp":25.5,"humidity":60.2,"pressure":1013.25,"comfort_index":85.0}
    ```
- Power Consumption:
  - Active/Measurement: ~152 mA
  - Idle/Sleep: ~60 µA
  - Communication Active (UART + HTTP): ~162 mA

## Mechanical

- Dimensions:
  - ~100 × 80 mm (breadboard)
  - Sensor Module: ~25 × 15 mm
- Weight: ~50 g
- Mounting Options: Breadboard compatible
- Materials: PCB core, potential plastic/metal enclosure

## Environmental

- Operating Temperature: -40 to +80°C
- Storage Temperature: -50 to +100°C
- Humidity: 0 to 100% RH (non-condensing)
- Pressure: 300 to 1100 hPa
- Environmental Ratings: No information

## Extra Information

- Compliance: Placeholder: Expected RoHS, CE, FCC compliance.  Verify with Distributed System Lab, Okayama University
- Troubleshooting: Refer to the troubleshooting table in the datasheet.

```

**Notes and Ambiguity Flags:**

*   In the section `Manufacturer Information`, the contact detail redirects to university administration rather than a direct support or contact.

*   For the Environmental section, the datasheet lacks standardized IP ratings or specific environmental certifications, I have marked these "No information"

I have attempted to extract and structure all the information as per your specifications. Let me know if you have another datasheet for me to process!