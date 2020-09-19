# SSD1306-i2c-esp-idf
A C++ driver for the i2c variant of the SSD1306 OLED display module for the ESP32 IDF

## Rationale
Why am I writing yet another driver for the SSD1306? Because I can, and because none of the existing drivers I have found worked the way I wanted them to. I needed a driver that would work with other I2C components on the same bus, so I initially picked the driver from the [Espressif IOT Solution Library](https://github.com/espressif/esp-iot-solution). This, however, does not have the features of other drivers I have seen, notably [Tara K's library](https://github.com/TaraHoleInIt/tarablessd1306). Most of these drivers also have code for other OLED driver chips and other connection protocols, stuff I don't want and need that gets in the way of my project. 

So this is my clean-slate remix of Espressif's and Tara K's libraries. It uses Espressif's I2CBus, but uses code from Tara K's library for font and text handling. It is designed solely for the I2C version of the SSD1306 OLED display module. It's purely C++, apart from the ESP IDF library calls. 

