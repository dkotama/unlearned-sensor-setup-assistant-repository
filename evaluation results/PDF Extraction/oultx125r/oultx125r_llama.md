## Key Specifications
* Part Number: OULTX125R
* Description: Dual-Light Sensor System for intelligent environmental sensing
* Key Features: Accurate measurement of ambient and directional light intensity, compact form factor, low power consumption, flexible connectivity options

## General Description
The OULTX125R is a cutting-edge dual-light sensor system designed for modern IoT deployments. It measures both ambient light levels and specific directional light intensity, making it suitable for various smart applications, including home automation, energy management, and security infrastructures. The device leverages the capabilities of an ESP32 DevKitC microcontroller for reliable data acquisition and provides a standardized digital output on GPIO13 for easy integration with external control units.

## Manufacturer Information
* Company Name: Not available
* Contact Details: For specific supplier details, please reach out directly to your sales representative
* Product Identification Details: Part Number - OULTX125R

## Performance
* Resolution: 12-bit Analog-to-Digital Converter (ADC) with 4095 distinct values
* Accuracy (post-calibration): Typically within ±5%
* Sampling Rate: Default 1 Hz, configurable to meet specific application requirements
* Latency: Less than 50 milliseconds
* Response Time: Under 10 milliseconds

## Electrical
* Power Supply: 
  - Operating Voltage: 3.3V DC or 5V DC
  - Power Consumption: Less than 500mW
  - Primary Power Method: 5V DC via ESP32's integrated USB Type-C port (minimum current: 500mA)
  - Alternative Power Method: 5V DC via ESP32's VIN pin (recommended current: 500mA)
* Control Voltage: Not specified
* Output Type: 
  - Digital Output: 3.3V HIGH signal or 0V LOW on GPIO13
  - Analog Output (Raw Sensor Data): 0-3.3V, mapped to digital values from 0-4095
* Interface Options: 
  - External Controller Integration: Seamless integration via GPIO13 digital output
  - Debugging & Monitoring: UART Serial interface over USB Type-C connection (baud rate: 115200)
* Data Output: 
  - Format: UART Serial Cable via USB Type-C port, streaming detailed sensor readings
  - Example:
    ```
    Ambient: <value> | Directional: <value> | Diff: <value> | Output Pin 13: <HIGH/LOW>
    ```
    Sample outputs:
    ```
    Ambient: 1500 | Directional: 3500 | Diff: 2000 | Output Pin 13: HIGH
    Ambient: 2000 | Directional: 1950 | Diff: 50 | Output Pin 13: LOW
    ```

## Mechanical
* Dimensions: 
  - ESP32 DevKitC Module: Approximately 50mm x 25mm
  - Individual Sensor Module: 20mm x 15mm
* Weight: Approximately 25 grams
* Mounting Options: Not specified
* Materials: Not specified

## Environmental
* Operating Temperature Range: -20°C to +60°C
* Storage Temperature: Not specified
* Environmental Ratings: IP20 rating, suitable for indoor environments
* Vibration Resistance: Not specified
* Humidity: Operational effectiveness maintained within 10% to 90% relative humidity (non-condensing)

## Extra Information
* Compliance with Standards: CE and FCC certifications, RoHS Compliant
* Troubleshooting Guide: Provided for common issues, including no serial output, saturated sensor readings, LEDs not lighting up, no GPIO13 output, and unstable readings