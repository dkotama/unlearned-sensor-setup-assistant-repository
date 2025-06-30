# OU-PWM48 Smart PID Control Sensor Datasheet

## Key Specifications
- High-precision water temperature monitoring
- PWM output for heating element control
- MQTT communication interface
- Compact, durable design
- IP65 water-resistant
- CE and RoHS compliant

## General Description
The OU-PWM48 Smart Sensor is an advanced, compact device designed for precise monitoring and Proportional-Integral-Derivative (PID) control of water heater systems. It acts as a standalone PID controller, calculating control actions internally and delivering real-time Pulse Width Modulation (PWM) output directly to water heater heating elements. The sensor enables efficient temperature regulation for smart home and industrial heating applications.

## Manufacturer Information
- Company: Okayama University
- Contact Email: darma.kotama@s.okayama-u.ac.jp
- Phone: +81-86-251-7047
- Support Hours: Monday-Friday, 9AM-5PM JST
- Part Number: OU-PWM48

## Performance
- Temperature Control Accuracy: ±1.0°C of target temperature
- Temperature Measurement Accuracy: ±0.5°C
- Ambient Compensation: ±2% accuracy
- Latency: <10 ms delay after sampling
- Response Time: Temperature sampling and MQTT transmission within 1 second
- Sampling Rate: Configurable, default 1 Hz

## Electrical
- Power Supply: 5V DC (USB) or 3.3V-5V DC (external regulated)
- Current Draw: 
  - Active: 25 mA
  - Idle: 5 mA
- Output Type: PWM Duty Cycle (0-100%)
- PWM Frequency: 1 kHz (configurable)
- Interface: MQTT

- Data Output:
  - Format: JSON via MQTT
  - Topics:
    - Data Publication: `ou/pwm48/<device_id>/data`
    - Status Publication: `ou/pwm48/<device_id>/status`
    - Command Subscription: `ou/pwm48/<device_id>/cmd`

- Example Data Payload:
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
- Dimensions: 50 mm × 35 mm × 15 mm
- Weight: Approximately 25 g
- Mounting: Two integrated mounting tabs for screw-based attachment
- Sensor Probe: Designed for thermal contact with water heater

## Environmental
- Operating Temperature Range: -20°C to +60°C
- Storage Temperature Range: -40°C to +85°C
- Ingress Protection: IP65 (water-resistant enclosure)
- Expected Lifespan: >5 years in typical conditions

## Extra Information
- Certifications: CE, RoHS compliant
- Warranty: 1-year limited warranty
- Security: Supports TLS/SSL encrypted MQTT communication
- Firmware Updates: Available through Okayama University support portal

**Ambiguity Alert:**
- Operating temperature range in datasheet shows conflict: Section 3 lists 0°C to +60°C, while other sections mention -20°C to +60°C. Recommend clarifying the exact operating range with manufacturer.