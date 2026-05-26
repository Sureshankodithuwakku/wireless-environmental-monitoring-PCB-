# wireless-environmental-monitoring-PCB-
Compact wireless environmental monitoring PCB built around the ESP32-S3-WROOM, with an onboard BME280 sensor.


No external modules. No jumper wires. Everything integrated directly on the board temperature, humidity, and barometric pressure sensing alongside the MCU in a single clean package.

The board transmits real-time environmental data over WiFi, making it suitable for smart home automation, industrial cold chain monitoring, greenhouse control, HVAC feedback systems, and beyond.

Key design decisions included:
→ Onboard BME280 for true all-in-one sensing
→ USB-C for power and programming
→ AMS1117 LDO regulator for a clean 3.3V supply
→ Dedicated reset button and status LEDs
→ 4-layer routing with proper ground planes
→ Fully designed and verified in Altium Designer

A production-ready PCB always comes down to the details:
✔ Component placement
✔ Trace routing
✔ Decoupling
✔ Design rule checks

"Isn't the ESP32 going to heat up the sensor?"
Yes, it can. The ESP32 generates heat during WiFi activity and processing, which can cause the BME280 to read 2–5°C above true ambient temperature.

But here's the thing 
✔ Humidity and pressure readings are completely unaffected
✔ Deep sleep mode dramatically reduces self-heating
✔ A wake → read → transmit firmware sequence minimises the error window
✔ A software calibration offset corrects for the remaining delta

