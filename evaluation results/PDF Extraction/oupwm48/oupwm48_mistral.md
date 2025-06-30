## Key Specifications Summary
-  Model: OU-PWM48
-  Purpose:  PID Control of Water Heaters
-  Type:  Advanced, Compact Water Temperature Sensor
  -  Accuracy: ±0.5°C for water temperature with ±2% ambient compensation
-  Operating Range: -20°C to +60°C
- PWM Frequency: 1 kHz (Configurable)
- Certifications: CE, RoHS

## General Description
The  OU-PWM48 Smart Sensor is an advanced, compact device designed for precise monitoring and Proportional-Integral-Derivative (PID) control of water heater systems. It operates as a standalone PID controller, calculating the necessary control action internally and delivering a real-time Pulse Width Modulation (PWM) output directly to the water heater's heating element. This enables efficient and reliable water temperature regulation, engineered for seamless integration into smart home and industrial heating applications. The sensor offers robust performance with a user-friendly interface.

**Key Features:**
-  High-precision water temperature monitoring.
-  Ambient condition compensation for optimized control.
-  Integrated PID controller for autonomous temperature regulation.
-  Direct PWM output for controlling water heater heating elements.
-  MQTT communication interface for easy integration with external systems, allowing for remote monitoring and PID parameter configuration.
-  Configurable target temperature and sampling rate.
-  Compact and durable design for versatile installation.

## Manufacturer Information
**Company Name**: Okayama University
- **Contact Details**: Supply support: darma.kotama@s.okayama-u.ac.jp | Research Collaboration: info_discovery@adm.okayama-u.ac.jp | Phone: +81-86-251-7047
- **Product Identification**:
    - Part Number:  OU-PWM48
    - **Customer Service**: Customer service hours are Monday to Friday.

## Performance
- **Speed**:  Temperature sampling and MQTT data transmission completed within 1 second (at 1 Hz).
- **Accuracy**: ±1°C for temperature control (with PID tuning) | Measurement Accuracy: ±0.5°C
- **Precision**:
    - **Ambient Compensation**:
        ```plaintext
- Adjusts for environmental conditions within ±2% accuracy.
- Minimizes the impact of surrounding temperature fluctuations on water temperature measurements.
```
   - **Latency**:  Real-time data output with <10 ms delay after sampling;  PWM output reacts continuously to PID calculations.
## Electrical
- **Power Supply**:  3.3V-5V DC (external power with regulator) | 5V DC (via USB)
- **Control Voltage**:  N/A
- **Output Type**:  PWM Duty Cycle (0-100%) for heating element control
  - **Current Draw**:  25 mA (Active); 5 mA (Idle)
- **Interface**:  MQTT
- **Data Output** :
- **Format**:  MQTT, JSON payload.
- **Example**:
```
Data Publication:  ou/pwm48/<device_id>/data

Example:
{"current_temp": 54.75, "target_temp": 55.0, "error": 0.25,  "pwm_duty_cycle": 75.0,  "ambient_comp": 22.5}

Status Publication:  ou/pwm48/<device_id>/status

Example:
{
    "status": "online",
    "uptime_s": 3600,
    "current_pwm_freq_hz": 1000
}

Command Subscription:  ou/pwm48/<device_id>/cmd

Example:
{
    "command": "SET_TARGET",
    "value": 50.0
}
```

## Mechanical
-  **Dimensions**:  50 mm x 35 mm x 15 mm (compact module)
-  **Weight**: Approx. 25 grams
-  **Mounting Options**:  Two integrated mounting tabs for screw-based attachment.
-  **Materials**: (No specific material mentioned)

## Environmental
- **Operating Temperature**: -20°C to +60°C
- **Storage Temperature**: -40°C to +85°C
- **Environmental Ratings**:  Water-resistant enclosure for sensor probe (IP65)
-  **Vibration Resistance**:  (No specific information provided)

- **Expected Lifespan**: >5 years in typical operating conditions.

## Extra Information
-  **Compliance with Standards/ Certifications**:  CE, RoHS.
-  **Troubleshooting Guide**:
```
Issue  Possible Cause  Solution
1.  No data output / No PWM control  Loose connections or power failure   Check power supply and connections.
2.  Inaccurate temperature control   Improper sensor placement; Incorrect PID tuning   Ensure the sensor probe is in good thermal contact. Adjust PID parameters (Kp, Ki, Kd) via MQTT.
3.  No PWM output signal   Incorrect wiring to heating element driver; PWM frequency misconfiguration    Verify PWM output pin is correctly wired to the heating element driver. Check PWM frequency setting.
4.  No MQTT data   Incorrect broker address/port, network issues, invalid topics, authentication failure  Verify network connectivity, MQTT broker settings, topic subscriptions, and credentials.
5.  Sensor not responding   Environmental stress or hardware fault   Ensure operating conditions are within −20°C to +60°C; contact supplier for further assistance.
```
- **Additional Resources**:

```
User Manual: Comprehensive setup and configuration guide provided with purchase
Support: Email: darma.kotama@s.okayama-u.ac.jp | Phone: +81-86-251-7047
Community Resources: Technical forums and user guides through Okayama University's Global Discovery Program
Warranty: 1-year limited warranty; contact darma.kotama@s.okayama-u.ac.jp for details or to initiate a claim.
```

- **Ambiguities or Conflicting Information**:
    - In Section 6.1 Accuracy and Precision, it is mentioned the accuracy of the water temperature measurement is ±0.5°C, yet in Section 4.2.1 MQTT Protocol, "Data Publication" example temperature includes a decimal value.
    - No specific details on the device material were described within the text.
    - There is no mention of vibration or shock resistance for the device.