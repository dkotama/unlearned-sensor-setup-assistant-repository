# OULTX125R - Dual-Light Sensor System - Data Sheet Summary

## Key Specifications

*   Dual-light sensor system for ambient and directional light intensity measurement.
*   Designed for IoT deployments in home automation, energy management, and security.
*   Utilizes an ESP32 DevKitC microcontroller for data acquisition.
*   Provides digital output on GPIO13 for easy integration.
*   Features three LED indicators for real-time status feedback.

## General Description

*   The OULTX125R is a dual-light sensor system designed for accurate measurement of ambient and directional light intensity. It leverages an ESP32 DevKitC microcontroller for data acquisition and provides digital output on GPIO13. The system is compact, low power, and suitable for diverse environmental monitoring projects.

## Manufacturer Information

*   Company Name: Not specified in current document.
*   Contact Details: For bulk orders or custom configurations of the OULTX125R, please reach out directly to your sales representative.
*   Product Identification:
    *   Model Number: OULTX125R

## Performance

*   Speed:
    *   Sampling Rate: 1 Hz (configurable)
    *   Latency: &lt; 50 milliseconds
    *   Response Time: &lt; 10 milliseconds
*   Accuracy: ±5% (post-calibration)
*   Precision:
    *   Resolution: 12-bit ADC (0-4095 values)

## Electrical

*   Power Supply:
    *   Operating Voltage: 3.3V DC or 5V DC
    *   Power Consumption: &lt; 500mW
    *   Primary Power Method: 5V DC via USB Type-C port (500mA minimum)
    *   Alternative Power Method: 5V DC via ESP32's VIN pin (500mA minimum)
*   Control Voltage: No information
*   Output Type:
    *   Digital Output: 3.3V HIGH / 0V LOW on GPIO13
    *   Analog Output: 0-3.3V (raw sensor data)
*   Interface:
    *   External Controller Integration: GPIO13 digital output (e.g., Raspberry Pi, Arduino)
    *   Debugging & Monitoring: UART Serial over USB Type-C (115200 baud)
*   Data Output:
    *   Format: Ambient: &lt;value> | Directional: &lt;value> | Diff: &lt;value> | Output Pin 13: &lt;HIGH/LOW>
    *   Example:
    ```
    Ambient: 1500 | Directional: 3500 | Diff: 2000 | Output Pin 13: HIGH
    Ambient: 2000 | Directional: 1950 | Diff: 50 | Output Pin 13: LOW
    ```

## Mechanical

*   Dimensions:
    *   ESP32 DevKitC Module: Approximately 50mm (length) x 25mm (width)
    *   Individual Sensor Module: 20mm x 15mm
*   Weight: Approximately 25 grams
*   Mounting Options: Specific mounting options are not detailed in this revision.
*   Materials: Information regarding specific materials used is currently unavailable.

## Environmental

*   Operating Temperature: -20°C to +60°C
*   Storage Temperature: No information
*   Environmental Ratings: IP20 (suitable for indoor environments)
*   Vibration Resistance: No information
*   Humidity: 10% to 90% relative humidity (non-condensing)

## Extra Information

*   Compliance: CE and FCC certifications (for the embedded ESP32 module), RoHS Compliant
*   Troubleshooting:
    *   No Serial Output Observed on Raspberry Pi
    *   Sensor Readings Appear Saturated (Constantly Showing 4095)
    *   LEDs Are Not Lighting Up
    *   No GPIO13 Output
    *   Unstable Readings Observed