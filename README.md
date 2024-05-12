# esp32-oled-rtd

This Arduino sketch demonstrates the use of an Adafruit MAX31865 PT100 sensor along with an SSD1306 OLED display. The sensor is used to measure temperature, and the measured values are displayed on the OLED screen.

## Hardware Components
- Adafruit MAX31865 PT100 Sensor
- SSD1306 OLED Display
- Arduino Board

## Libraries Used
- Adafruit_MAX31865: Used to interface with the MAX31865 PT100 sensor.
- Adafruit_GFX: Graphics library for the OLED display.
- Adafruit_SSD1306: OLED display library.

## Pin Configuration
- MAX31865:
  - CS: Pin 5
  - DI: Pin 23
  - DO: Pin 19
  - CLK: Pin 18
- OLED Display:
  - SDA: A4 (SDA pin)
  - SCL: A5 (SCL pin)

## Description
1. Initialize serial communication at 115200 baud rate.
2. Initialize the MAX31865 sensor in 3-wire mode.
3. Initialize the OLED display.
4. Display an initial message on the OLED screen.
5. Continuously read temperature from the sensor.
6. Print temperature values and any faults detected by the sensor via serial monitor.
7. Display the temperature readings on the OLED screen along with a header.
8. Implement a scrolling text animation on the OLED screen.

## Functions
- `setup()`: Initialize serial communication, sensor, OLED display, and draw initial display contents.
- `loop()`: Continuously read temperature, print values, clear display, and update OLED with temperature readings.
- `testscrolltext()`: Scroll text on the OLED screen.

## Additional Notes
- The code uses software SPI for the MAX31865 sensor.
- The OLED display is set up using I2C communication.
- The sketch includes functions to draw basic shapes and perform scrolling text animation on the OLED screen.
- Make sure to adjust the pin configurations according to your hardware setup.

