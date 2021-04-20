# Adafruit Uncanny Eye on ESP32 NTSC Composite Video

## The idea:

A = Color composite video code from __rossumer__'s
[ESP_8_BIT project](https://github.com/rossumur/esp_8_bit)
, extracted at
[my fork](https://github.com/Roger-random/esp_8_bit.git).

B = __Adafruit__'s
[Uncanny Eyes](https://github.com/adafruit/uncanny_eyes) project.

A + B = Uncanny Eye on a NTSC TV via composite video, running on an ESP32

## The execution:

The interesting challenge was to see if A and B can run together.
I have enough to prove the concept for answer of "yes", and I find I have
little enthusiasm to finish it the rest of the way.

Incomplete list of fixes to do:

The eye runs in full automatic random mode. (Random movement, random blink,
random iris.) Need fixes to hardware interface for joystick movement,
blink button, and iris light sensor.

Eye is displayed in the center 128x128 of frame buffer. Need image scaling
code to correct for (1) nonsquare pixels (eye is oval instead of circular)
and (2) expand to fill more of the screen.
