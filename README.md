#  EspHome configurations for MyStrom devices

| Device         | Config                                             |
| :------------- | :------------------------------------------------- |
| WiFi Switch V1 | Not supported, incompatible chipset.               |
| WiFi Switch V2 | [mystrom-switch-v2.yaml](./mystrom-switch-v2.yaml) |

##  WiFi Switch v2

ESPHome support for the MyStrom V2 Wifi Switch. Currently the following features are supported

- Control the relay
- Control the red and white LED
- Side and bottom buttons (same function)
- Energy monitoring and reporting (room for improvement)
- Reading the internal temperature sensor
- Emergency power off if the internal temperature is to high

### WiFi Switch Pinout

```txt
      JP1
GND   [] ()   TXD
GND   () ()   RXD
GND   () ()   GPIO0
GND   () ()
GND   () ()
VCC   () ()
VCC   () ()
      () ()
      () ()
```

###  Flashing

Connect a UART programmer to the WiFi Switch in the following way:

| MyStrom PIN | Programmer |
| ----------- | :--------: |
| GND         |    GND     |
| VCC         |    3V3     |
| TXD         |    TXD     |
| RXD         |    RXD     |
| GPIO0       |    GND     |

If you use dupont wires it may be possible to connect these without soldering.
