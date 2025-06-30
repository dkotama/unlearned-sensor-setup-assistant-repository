# OU-PWM48 Smart PID Control Datasheet - Extracted Information

## Key Specifications

*   High-precision water temperature monitoring.
*   Ambient Condition compensation for optimized control.
*   Integrated PID controller for autonomous temperature regulation.
*   Direct PWM output for controlling water heater heating elements.
*   MQTT communication interface for remote monitoring and parameter configuration.
*   Configurable target temperature and sampling rate.
*   Compact and durable design.

## General Description

-   The OU-PWM48 Smart Sensor is designed for precise monitoring and PID control of water heater systems.
-   It acts as a standalone PID controller, calculating the necessary control action internally and delivering a real-time PWM output directly to the water heater's heating element.
-   It enables efficient and reliable water temperature regulation.
-   It's engineered for seamless integration into smart home and industrial heating applications.
-   It offers robust performance with a user-friendly interface.

## Manufacturer Information

-   **Company:** Okayama University (Collaboration)
-   **Contact Emails:**
    -   darma.kotama@s.okayama-u.ac.jp (For pricing, availability, support, and warranty)
    -   info_discovery@adm.okayama-u.ac.jp (For research partnerships)
-   **Contact Number[s]:** +81-86-251-7047 (Available 9AM-5PM JST, Monday-Friday).
-   **Product Identification:** OU-PWM48 (Part Number)
-   **Website**: Okayama University Support Portal (Firmware Updates)

## Performance

-   Temperature Control Accuracy: ±1.0°C of the target temperature (under stable load conditions, depends on PID tuning).
-   Temperature Measurement Accuracy: ±0.5°C (water temperature).
-   Ambient Compensation Accuracy: ±2%.
-   Latency: <10 ms delay after sampling; PWM output reacts continuously to PID calculations.

## Electrical

-   Power Supply: 5V DC (via USB) or 3.3V-5V DC (external power with regulator)
-   Typical Current Draw:  25 mA (Active); 5 mA (Idle)
-   Output: PWM Duty Cycle (0-100%) for heating element control
-   PWM Frequency: 1 kHz (Configurable)
-   Interface: MQTT (configurable broker and topics)
-   Data Output:
    - Format: JSON via MQTT
    - Example:
```json
{
    "current_temp": 54.75,
    "target_temp": 55.0,
    "error": 0.25,
    "pwm_duty_cycle": 75.0,
    "ambient_comp": 22.5
}
```

## Mechanical

-   Dimensions: 50 mm × 35 mm × 15 mm (compact module)
-   Weight: Approx. 25 g
-   Mounting: Two integrated mounting tabs for screw-based attachment.
-   Materials: No information

## Environmental

-   Operating Temperature Range: -20°C to +60°C
-   Storage Temperature Range: -40°C to +85°C
-   Ingress Protection: IP65 (water-resistant enclosure for sensor probe)
-   Vibration Resistance: No information

## Extra Information

-   Certifications: CE, RoHS compliant
-   Expected Lifespan: >5 years in typical operating conditions.
-   MQTT Security:
    -   TLS/SSL (Port 8883): Supports encrypted connections to the MQTT broker.
    -   Authentication: Supports username/password authentication (contact supplier for details).
- Troubleshooting:
    - Issue: No data output / No PWM control
       - Possible Cause: Loose connections or power failure
       - Solution: Check power supply and connections.
    - Issue: Inaccurate temperature control
       - Possible Cause: Improper sensor placement; Incorrect PID tuning
       - Solution: Ensure the sensor probe is in good thermal contact. Adjust PID parameters (Kp, Ki, Kd) via MQTT.
    - Issue: No PWM output signal
       - Possible Cause: Incorrect wiring to heating element driver; PWM frequency misconfiguration
       - Solution: Verify PWM output pin is correctly wired to the heating element driver. Check PWM frequency setting.
    - Issue: No MQTT data
       - Possible Cause: Incorrect broker address/port, network issues, invalid topics, authentication failure
       - Solution: Verify network connectivity, MQTT broker settings, topic subscriptions, and credentials.
    - Issue: Sensor not responding
       - Possible Cause: Environmental stress or hardware fault
       - Solution: Ensure operating conditions are within −20∘C to +60∘C; contact supplier for further assistance.

**Ambiguity/Conflicting Information:**

*   The datasheet mentions a configurable PWM frequency of 1 kHz initially, but Example Configuration Commands has an entry to set the PWM Frequency to *2000* Hz in Section 4.2.1. Communication Protocol.
* The operating temperature ranges throughout the document. The troubleshooting section lists an operating range of -20C to +60C, whereas in the technical specifications section it lists 0C to +60C.
