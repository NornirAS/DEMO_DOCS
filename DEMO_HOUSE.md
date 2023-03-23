# Demo house

## Domains

demohouse.cioty.com

## Services

### esp32gw

Represent ESP32 micro-controller inside the house. should link to APP service to receive the commands.

```xml
<RTW>
<SENDER></SENDER>
<PAYLOAD></PAYLOAD>
<COMMAND>@DEMOHOUSE/UI#COMMAND@</COMMAND>
</RTW>
```

### Ghosts

This service should have two ghosts, one for each ESP32. Each of those ghosts should have 1 morphed ghost: demohouse.cioty.com/ui##1

### ui

This is the UI service with a floor plan. It should link to GW service and receive data from the sensors.

```xml
<RTW>
<SENDER></SENDER>
<PAYLOAD>@DEMOHOUSE/ESP32#PAYLOAD@</PAYLOAD>
<COMMAND></COMMAND>
</RTW>
```

## Ghosts

This service should have a 1 ghost. It should have 2 morphed ghosts: demohouse.cioty.com/esp32gw##1 and demohouse.cioty.com/esp32gw##2.

## Project Links

[UI](https://github.com/NornirAS/demo-house-ui)

[BACKEND](https://github.com/NornirAS/demo-house-backend)
