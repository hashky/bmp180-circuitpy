# bmp180-circuitpy
Port of adafruit python bmp legacy code to current circuitpython 7 busio

original repo https://github.com/adafruit/Adafruit_Python_BMP

'''
import bmp180
import board
import busio as io

i2c = io.I2C(board.SCL,board.SDA)

bmp = bmp180.BMP085(i2c=i2c)
bmp.read_temperature()
bmp.read_altitude()
bmp.read_pressure()                 
'''
