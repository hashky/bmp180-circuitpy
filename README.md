# bmp180-circuitpy
Port of adafruit python bmp085/bmp180 pressure and temperature sensor legacy code to current circuitpython 7 busio. bmp180 is deprecated/discontinued hardware and replaced by bmp280, Th i2c interface is not backwards compatible. This seemed like an inconsiderate design decision until i saw the ammount of calculations you have to deal with on the i2c master when i ported this code.... 

hope this helps someone make use of some cheap obsolete chips

original repo https://github.com/adafruit/Adafruit_Python_BMP

```py
import bmp180
import board
import busio as io

i2c = io.I2C(board.SCL,board.SDA)

bmp = bmp180.BMP085(i2c=i2c)
bmp.read_temperature()
bmp.read_altitude()
bmp.read_pressure()                 
```
