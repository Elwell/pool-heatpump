# Modbus interface for Pool Heatpump
Pulling information from a Madimack branded pool heatpump into home assistant. No cloud needed.


## Background
We have a 9kW heat-only heat pump attached to a basic spa plunge pool controller. It's wired so that the main power for the heat pump comes from the controller with the existing heating element disconnected and used to trigger a relay connected to the heat pump external trigger (volt free, digital in 2)

The heat pump seems to be a rebranded Fairland model which came with a tuya wifi module on the back. There's a fairly good thread at https://community.home-assistant.io/t/controlling-a-fairland-pool-heatpump-eliminating-tuya/579467 with people contributing the modbus registers

## Prototype
Removed the supplied wifi adaptor off the back (slides off, has a M10 4 pin connector to carrying 12v, Gnd, RS485 A+B), re-used the cable onto a lilygo t-can485
https://github.com/Xinyuan-LilyGO/T-CAN485 and flashed with an ESPHome config


## Custom PCB
Aim is to replace the t-can board with a custom fabbed one that fits in the existing case

