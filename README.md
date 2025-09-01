# Variable-Soldering-Station
Turn an old iron into a temperature-controlled press using Arduino, a K-type thermocouple, MAX6675 amplifier, relay, buttons, and an I2C LCD.

# Features
  Accurate temperature measurement with a K-type thermocouple (up to 1024°C).
  
  Setpoint adjustment via increment/decrement buttons (2°C steps).
  
  Live temperature display on a 16x2 I2C LCD.
  
  Relay-based heater control keeps the iron at your target temperature.
  
  Safety first: relay is OFF by default at startup.

# Hardware Required
  Arduino (Uno, Nano, etc.)
  
  MAX6675 K-type thermocouple amplifier
  
  K-type thermocouple (0–1024°C, check your probe’s actual max temp)
  
  16x2 I2C LCD display (address 0x27)
  
  Relay module (to switch AC power to the iron)
  
  3 push buttons (increase, decrease, set)
  
  Repurposed iron (used as the heater)
  
  Assorted wires and connectors

# Circuit Diagram
  MAX6675 → Arduino: SCK (10), CS (11), SO (12)
  
  Relay signal → Pin 2
  
  LCD SDA/SCL → Arduino SDA/SCL
  
  Buttons → Pins 4 (inc), 5 (dec), 6 (set)
  
  Relay output in series with AC to iron

# Usage Instructions
  Make all hardware connections as above.
  
  Upload the Arduino code in this repo to your board.
  
  Power up—relay/heater is safely OFF by default.
  
  Use the buttons to set your desired temperature.

# LCD shows:

  First row: SET TEMP = <target>
  
  Second row: Temp cel= <actual>
  
  Iron heats when actual temp is below setpoint; turns off automatically when reached.

# Example Code
  See the code file in this repository.

# Safety Notes
  The MAX6675 supports up to 1024°C, but most cheap K-type probes are only safe up to ~450–800°C.
  
  Use proper insulation and an enclosure for all mains/relay wiring.
  
  Disconnect AC power before modifications.

# License
  MIT or your preferred open-source license.

# Credits
  Project inspired by open-source Arduino soldering iron and temperature controller designs.

