# Demo house

## Domains

demo-house.cioty.com

## Services

### esp32gw

Represent ESP32 micro-controller inside the house. should link to APP service to receive the commands.

```xml
<RTW>
<DEMO_DOOR></DEMO_DOOR>
<DEMO_LIGHT></DEMO_LIGHT>
<DEMO_FIRE></DEMO_FIRE>
<DEMO_DHT11></DEMO_DHT11>
<DEMO_CO2></DEMO_CO2>
<DEMO_PIR></DEMO_PIR>
<DEMO_FAN></DEMO_FAN>
<COMMAND>
  @DEMO/APP#COMMAND@
</COMMAND>
</RTW>
```

### Ghosts

This service should have two ghosts, one for each ESP32. Each of those ghosts should have 1 morphed ghost: demo-house.cioty.com/ui##1

### ui

This is the UI service with a floor plan. It should link to GW service and receive data from the sensors.

```xml
<RTW>
<PAYLOAD>
  @DEMO/GW#DEMO_DOOR@
  @DEMO/GW#DEMO_LIGHT@
  @DEMO/GW#DEMO_FIRE@
  @DEMO/GW#DEMO_DHT11@
  @DEMO/GW#DEMO_CO2@
  @DEMO/GW#DEMO_PIR@
  @DEMO/GW#DEMO_FAN@
</PAYLOAD>
<COMMAND></COMMAND>
</RTW>
```

## Ghosts

This service should have a 1 ghost. It should have 2 morphed ghosts: demo-house.cioty.com/esp32gw##1 and demo-house.cioty.com/esp32gw##2.