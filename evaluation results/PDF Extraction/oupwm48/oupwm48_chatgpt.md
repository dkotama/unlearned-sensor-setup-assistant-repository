# OU-PWM48 Smart Sensor Datasheet

## Key Specifications
- **High-precision water temperature monitoring**
- **Ambient condition compensation for optimized control**
- **Integrated PID controller for autonomous temperature regulation**
- **Direct PWM output for controlling water heater heating elements**
- **MQTT communication interface for integration with external systems**
- **Configurable target temperature and sampling rate**
- **Compact and durable design for versatile installation**

---

## General Description
The OU-PWM48 Smart Sensor is an advanced, compact device designed for precise monitoring and Proportional-Integral-Derivative (PID) control of water heater systems. It operates as a standalone PID controller, internally calculating the required control action and delivering real-time Pulse Width Modulation (PWM) output directly to the water heater's heating element. This ensures efficient and reliable water temperature regulation, designed for seamless integration into smart home and industrial heating applications, providing robust performance and a user-friendly interface.

---

## Manufacturer Information
- **Manufacturer:** Okayama University
- **Contact Email:** darma.kotama@s.okayama-u.ac.jp
- **Phone:** +81-86-251-7047
- **Website:** Not explicitly mentioned
- **Mailing Hours:** 9AM-5PM JST, Monday-Friday
- **Product Identifier:** OU-PWM48
- **Additional Support:** Comprehensive setup, firmware updates, and community resources available through Okayama University's programs.

---

## Performance
- **Accuracy:**
  - Water temperature measurement: ±0.5°C
  - Ambient condition compensation: ±2%
  - Temperature control accuracy: ±1.0°C under stable conditions
- **Response Time:**
  - Temperature sampling and MQTT transmission: <1 second (1 Hz default sampling rate)
  - PID calculation and PWM output updates: Real-time (<10ms delay after sampling)
- **Reliability:**
  - Designed for continuous operation in water heater environments
  - Features built-in error handling and IP65-rated sensor probe for water exposure
- **Other Details:** Configurable PID parameters (Kp, Ki, Kd) for precise temperature control.

---

## Electrical
- **Power Supply:**
  - 5V DC (via USB)
  - 3.3V-5V DC (external power option with regulator)
- **Typical Current Draw:**  
  - Active Mode: 25 mA  
  - Idle Mode: 5 mA  
- **Output Type:**  
  - PWM Duty Cycle (0-100%) for heating element control.
- **Interface:** MQTT via TCP/IP stack.
- **Data Output:**
  - **Format:** JSON payloads transmitted via MQTT topics:
    - Example Topic: `ou/pwm48/<device_id>/data`
    - Example Data: `{"current_temp":54.75,"target_temp":55.0,"error":0.25,"pwm_duty_cycle":75.0,"ambient_comp":22.5}`
  - Example MQTT broker settings for development:
    - Host: `broker.hivemq.com`
    - Port (Unencrypted): 1883
    - Port (TLS/SSL): 8883
- **Example Data Output:**  
  ```json
  {"current_temp": 54.75, "target_temp": 55.0, "error": 0.25, "pwm_duty_cycle": 75.0, "ambient_comp": 22.5}
  ```
- **Other Communication Protocols:** Supports secure MQTT over TLS/SSL with username/password authentication.
- **Configurable Parameters via MQTT Commands:**
  - Target temperature, sampling rate, PID parameters (Kp, Ki, Kd), and PWM frequency.

---

## Mechanical
- **Dimensions:** 50 mm × 35 mm × 15 mm
- **Weight:** Approx. 25g
- **Mounting Options:**
  - Screw-based attachment using integrated mounting tabs.
- **Material:** Not explicitly detailed.
- **Other Details:** Designed for compactness and versatile installation.

---

## Environmental
- **Operating Temperature Range:** -20°C to +60°C
- **Storage Temperature Range:** -40°C to +85°C
- **Environmental Rating:** IP65 rating for water-resistance
- **Vibration Resistance:** Not explicitly mentioned.

---

## Extra Information
- **Compliance:** CE and RoHS certifications
- **Troubleshooting Guide:** 
  - **No data output / No PWM control:** Check power supply and connections.
  - **Inaccurate temperature control:** Ensure proper sensor placement and adjust PID parameters via MQTT.
  - **No PWM output signal:** Verify wiring and PWM frequency setting.
  - **No MQTT data communication:** Confirm broker address, network settings, and credentials. 
  - **Sensor not responding:** Ensure operating conditions are within specified environmental ranges.
- **Safety Instructions:**
  - Use regulated power to prevent overvoltage.
  - Follow local regulations for water heater modifications and electrical wiring.
- **Advanced Support:** Available for integration requests or firmware updates.

---

## Ambiguities and Issues Detected
- **Material Details:** The datasheet does not mention the material composition of the sensor housing or probe.
- **Mechanical Specifications:** Vibration resistance details are absent, which might be critical for industrial applications.
- **Website for Resources:** Although the datasheet references a downloadable user manual and firmware updates, the official website for this information is not explicitly mentioned.
