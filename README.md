# python-magichue
Magichue is a cheap smart led bulb that you can controll hue/saturate/brightnes and power over WiFi. They are available at Amazon or other online web shop.

I tested this library with [this bulb](http://www.amazon.co.jp/exec/obidos/ASIN/B0777LXQ4R/).


# Example
Turn Magichue On/Off.
```python
import magichue


light = magichue.Light('192.168.0.20')  # change address

# Show power status
print(light.on)

# Turn On
light.on = True

# Turn Off
light.on = False

# Show current color 
print(light.rgb)  # => (95, 25, 128)
print(light.r)  # => 95
print(light.g)  # => 25
print(light.b)  # => 128

print(light.is_white)  # => whether warm white LED is using or not.
print(light.w)  # => brightness of warm white LED.

print(light.hue)  # => 0.7799352750809061
print(light.saturate)  # => 0.8046875
print(light.brightness)  # => 128


# Changing Color
# By rgb
light.rgb = (128, 64, 32)

# By individual rgb value
light.r = 255

# By hue/saturate/brightness
light.hue = 0.3
light.saturate = 0.6
light.brightness = 255

```

Other features are in development.
