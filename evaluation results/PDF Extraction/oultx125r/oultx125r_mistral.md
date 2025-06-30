## Key Specifications

- Type: Dual-Light Sensor System

- Light Range: Ambient and specific directional light intensity

## General Description

- Cutting-edge solution for intelligent environmental sensing.

- Dual-light sensor for accurate measurement of ambient and directional light levels.

- Suitable for smart home automation, energy management, and security infrastructures.

- Core based on ESP32 DevKitC microcontroller for reliable data acquisition.

- Provides a standardized digital output on GPIO13, promotes effortless integration with external control units like Raspberry Pi.

- Operational clarity enhanced through three distinct LED indicators.

- Compact form factor, low power consumption, and flexible connectivity options.

 **Note: The document seems to omit a clear purpose/key features section, only an overview.**
## Manufacturer Information
 **Note: the document lacks a clear company name**

- For information regarding bulk orders or custom configurations, contact your sales representative.

## Performance

- Resolution:
 - Captured using a 12-bit Analog-to-Digital Converter (ADC) offering values from 0 to 4095.

- Accuracy:
 - Typically within ±5% post-calibration.

- Sampling Rate:
 - Default data acquisition rate is 1 Hz, configurable for specific application requirements.

- Response Time:
 - Less than 10 milliseconds for detecting rapid changes in light.

- Latency:
  - Less than 50 milliseconds for real-time applications.

## Electrical

- Power Supply:
 - Operating Voltage: 3.3V DC or 5V DC
 - Primary Power Method: 5V DC via USB Type-C port, minimum current of 500mA.
 - Alternative Power Method: 5V DC through ESP32's VIN pin, recommended current of 500mA.
 - Power Consumption: Under 500mW under typical operating conditions
 - Control Voltage: Information not specified in the current documentation.

- Output Type:
  - Digital Output: 3.3V HIGH or 0V LOW on GPIO13
  - Analog Output: 0-3.3V, mapped through 12-bit ADC to digital values 0-4095.

- Interface:
  - Integration with microcontrollers via GPIO13 digital output.
  - UART Serial interface accessible over USB Type-C, baud rate 115200.

- Data Output:
  - Format: UART Serial Cable via USB Type-C port
  - Example:
    ```
    Ambient: <value> | Directional: <value> | Diff: <value> | Output Pin 13: <HIGH/LOW>

    Ambient: 1500 | Directional: 3500 | Diff: 2000 | Output Pin 13: HIGH
    Ambient: 2000 | Directional: 1950 | Diff: 50 | Output Pin 13: LOW
    ```
  - GPIO13 Output Behavior: High when calculated difference between ambient and directional light values exceeds 100; Low otherwise.

## Mechanical

- Dimensions:
 - ESP32 DevKitC Module: Approximately 50mm in length by 25mm in width *indicator of inaccuracy on part dimensions*
 - Individual Sensor Module: 20mm x 15mm
- Weight:
  - Approximately 25 grams (including all LEDs)

- Mounting Options:
  - No detailed information available for mounting options
 - Materials:
  - No material details available

  **Note: Determining exact weight requires correction for improperly assembled parts with potential duplicate weight measurement/occurance. *Misc.* Also, discrepancies in part dimensions.*
## Environmental

**Note: Temperature Expressions are reached only for particular ranges:**

- Operating Temperature: -20°C to +60°C

- Storage Temperature:
 - No specific storage temperature guidelines available

- Environmental Ratings:
 - IP20 rating
 - Protection from dust ingress but not from water ingress.

- Humidity:
  - Effective within a 10% to 90% non-condensing relative humidity range.

  - Vibration Resistance:
    - No information regarding vibration resistance available.

    **Note: Ambiguities arise on criteria/Results of IP20 Environmental ratings & conditions. Doubt of IP20 ratings being an abstraction/venacular. Clarification requested on IP20 owing issues for environmental rating's enforcement.**
## Extra Information

  - Certifications:
  - Adheres to CE, FCC standards for European and US regulatory requirements for electronic devices.
  - RoHS compliant.
    - Troubleshooting Guide:
 - Contact sales representative for common issues.

