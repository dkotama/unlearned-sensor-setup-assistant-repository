# Smart Environmental Sensor OUTTX-110 Datasheet

## Key Specifications
- **Manufacturer**: Distributed System Lab, Okayama University
- **Product Code**: SES-OUTTX-110-2025
- **Sensing Capabilities**: Temperature, Humidity, Atmospheric Pressure
- **Temperature Range**: -40 to +80°C
- **Humidity Range**: 0–100% RH
- **Pressure Range**: 300–1100 hPa
- **Outputs**: UART (CSV), HTTP POST (JSON)
- **Power**: 3.3V, Low-power operation

## Manufacturer Information
- **Name**: Distributed System Lab, Okayama University
- **Address**: 3-1-1 Tsushima-naka, Kita-ku, Okayama 700-8530, Japan
- **Website**: https://www.okayama-u.ac.jp/
- **Product Code**: SES-OUTTX-110-2025
- **Production Date**: Prototype Batch 2025-01, June 2025
- **Contact**: Email university administration for lab inquiries
- **Mission**: Advancing IoT solutions for environmental monitoring

## General Description
The OUTTX-110 is a compact, IoT-enabled environmental sensor that:
- Measures temperature, humidity, and atmospheric pressure
- Computes a Comfort Index to assess environmental quality
- Supports dual data output: UART and HTTP POST
- Features built-in web server for configuration
- Designed for smart homes, weather stations, and industrial monitoring
- Provides low-power operation with Wi-Fi connectivity

## Performance
- **Temperature**:
  - Range: -40 to +80°C
  - Accuracy: ±0.5°C
  - Resolution: 0.1°C
- **Humidity**:
  - Range: 0 to 100% RH
  - Accuracy: ±2% RH
  - Resolution: 0.1% RH
- **Pressure**:
  - Range: 300 to 1100 hPa
  - Accuracy: ±0.12 hPa
  - Resolution: 0.03 hPa
- **Response Time**: ~2 seconds
- **Stability**: <0.1% RH/year, <0.05 hPa/year

## Electrical
- **Power Supply**: 2.2V to 3.6V (3.3V typical)
- **Logic Levels**: 3.3V for UART and internal interfaces
- **UART Parameters**: 
  - Baud Rate: 115200
  - 8 data bits, no parity, 1 stop bit
- **Wi-Fi**: 2.4 GHz, 802.11 b/g/n
- **Power Consumption**:
  - Active/Measurement: ~152 mA
  - Idle/Sleep: ~60 µA
  - Communication Active: ~162 mA
- **Data Output**:
  - UART: CSV string (temp,humidity,pressure,comfort_index)
  - HTTP POST: JSON payload to configurable server

## Mechanical
- **Dimensions**: 
  - Breadboard: ~100 × 80 mm
  - Sensor Module: ~25 × 15 mm
- **Materials**: PCB core, potential plastic/metal enclosure
- **Weight**: ~50 g

## Environmental
- **Operating Temperature**: -40 to +80°C
- **Storage Temperature**: -50 to +100°C
- **Humidity**: 0 to 100% RH (non-condensing)
- **Pressure Range**: 300 to 1100 hPa

## Extra Information
- **Potential Applications**:
  - Home Automation
  - Weather Stations
  - Greenhouses
  - Smart Offices
  - Health Monitoring
- **Future Enhancements**:
  - HTTPS support
  - Authentication for HTTP POST
  - Battery-powered operation
  - IP54 enclosure
- **Compliance**: Expected RoHS, CE, FCC compliance (to be verified)

## Ambiguities/Conflicts
No significant ambiguities or conflicts were identified in the provided datasheet text.