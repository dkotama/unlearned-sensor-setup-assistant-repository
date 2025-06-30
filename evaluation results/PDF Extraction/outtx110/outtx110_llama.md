## Key Specifications
The Smart Environmental Sensor OUTTX-110 is a compact, IoT-enabled device that measures temperature, humidity, and atmospheric pressure, computing a Comfort Index to assess environmental quality.

## General Description
The Smart Environmental Sensor OUTTX-110 is a compact, IoT-enabled device that measures temperature, humidity, and atmospheric pressure, computing a Comfort Index to assess environmental quality. It supports dual data output: UART for local integration (e.g., Raspberry Pi) and HTTP POST for cloud/server integration. A built-in web server allows configuration of the target server IP, enhancing IoT flexibility.

## Manufacturer Information
- Manufacturer: Distributed System Lab, Okayama University
- Address: 3-1-1 Tsushima-naka, Kita-ku, Okayama 700-8530, Japan
- Website: https://www.okayama-u.ac.jp/
- Production Date: Prototype Batch 2025-01, June 2025
- Product Code: SES-OUTTX-110-2025
- Contact: Email university administration for lab inquiries; support available via research portal
- Mission: Advancing IoT solutions for environmental monitoring, emphasizing reliability, scalability, and user-centric design
- Support Process: Technical support via research portal, typically within 48 hours for prototype inquiries

## Performance
- Temperature:
  - Range: -40 to +80°C
  - Accuracy: ±0.5°C
  - Resolution: 0.1°C
- Humidity:
  - Range: 0 to 100% RH
  - Accuracy: ±2% RH
  - Resolution: 0.1% RH
- Pressure:
  - Range: 300 to 1100 hPa
  - Accuracy: ±0.12 hPa
  - Resolution: 0.03 hPa
- Comfort Index:
  - Range: 0 to 100
  - Formula: 100 - (|temp - 22| * 2 + |humidity - 50| * 1.5 + |pressure - 1013| * 0.05)
- Response Time: ~2 seconds
- Stability: <0.1% RH/year, <0.05 hPa/year

## Electrical
- Power Supply: 2.2V to 3.6V (3.3V typical)
- Logic Levels: 3.3V for UART and internal interfaces
- UART Parameters: 115200 baud, 8 data bits, no parity, 1 stop bit
- Wi-Fi: 2.4 GHz, 802.11 b/g/n
- Signal Integrity: Low noise, stable output
- Data Output:
  - Format: UART (CSV) and HTTP POST (JSON)
  - Example (UART): 25.5,60.2,1013.25,85.0
  - Example (HTTP POST): {"temp":25.5,"humidity":60.2,"pressure":1013.25,"comfort_index":85.0}

## Mechanical
- Dimensions: ~100 × 80 mm (breadboard)
- Sensor Module: ~25 × 15 mm
- Materials: PCB core, potential plastic/metal enclosure
- Weight: ~50 g
- Mounting Options: Breadboard-based prototype

## Environmental
- Operating Temperature: -40 to +80°C
- Storage Temperature: -50 to +100°C
- Humidity: 0 to 100% RH (non-condensing)
- Pressure: 300 to 1100 hPa
- Environmental Ratings: No specific ratings provided

## Extra Information
- Compliance and Certifications: Expected RoHS, CE, FCC compliance (verify with Distributed System Lab, Okayama University)
- Troubleshooting Guide: Provided in the datasheet, including steps for no UART output, no HTTP POST, erratic readings, and more
- Integration Examples: Cloud (e.g., ThingSpeak), Smart Home (e.g., Home Assistant), Server Logging
- Future Enhancements: HTTPS support, authentication for HTTP POST, battery-powered operation, IP54 enclosure for rugged environments

No ambiguous or conflicting information was found in the provided text.