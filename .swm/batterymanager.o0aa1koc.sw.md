---
id: o0aa1koc
title: BatteryManager
file_version: 1.1.3
app_version: 1.12.1
---

The BatteryManager class contains strings and constants used for values in the `Intent.ACTION_BATTERY_CHANGED` Intent, and provides a method for querying battery and charging properties.

<br/>

|### Constants|                                                                                                                                                                                                                            |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`String`     |`ACTION_CHARGING`<br><br>Sent when the device's battery has started charging (or has reached full charge and the device is on power).                                                                                       |
|`String`     |`ACTION_DISCHARGING`<br><br>Sent when the device's battery may be discharging, so apps should avoid doing extraneous work that would cause it to discharge faster.                                                          |
|`int`        |`BATTERY_HEALTH_COLD`<br><br><br/>                                                                                                                                                                                          |
|`int`        |`BATTERY_HEALTH_DEAD`<br><br><br/>                                                                                                                                                                                          |
|`int`        |`BATTERY_HEALTH_GOOD`<br><br><br/>                                                                                                                                                                                          |
|`int`        |`BATTERY_HEALTH_OVERHEAT`<br><br><br/>                                                                                                                                                                                      |
|`int`        |`BATTERY_HEALTH_OVER_VOLTAGE`<br><br><br/>                                                                                                                                                                                  |
|`int`        |`BATTERY_HEALTH_UNKNOWN`<br><br><br/>                                                                                                                                                                                       |
|`int`        |`BATTERY_HEALTH_UNSPECIFIED_FAILURE`<br><br><br/>                                                                                                                                                                           |
|`int`        |`BATTERY_PLUGGED_AC`<br><br>Power source is an AC charger.                                                                                                                                                                  |
|`int`        |`BATTERY_PLUGGED_DOCK`<br><br>Power source is dock.                                                                                                                                                                         |
|`int`        |`BATTERY_PLUGGED_USB`<br><br>Power source is a USB port.                                                                                                                                                                    |
|`int`        |`BATTERY_PLUGGED_WIRELESS`<br><br>Power source is wireless.                                                                                                                                                                 |
|`int`        |`BATTERY_PROPERTY_CAPACITY`<br><br>Remaining battery capacity as an integer percentage of total capacity (with no fractional part).                                                                                         |
|`int`        |`BATTERY_PROPERTY_CHARGE_COUNTER`<br><br>Battery capacity in microampere-hours, as an integer.                                                                                                                              |
|`int`        |`BATTERY_PROPERTY_CURRENT_AVERAGE`<br><br>Average battery current in microamperes, as an integer.                                                                                                                           |
|`int`        |`BATTERY_PROPERTY_CURRENT_NOW`<br><br>Instantaneous battery current in microamperes, as an integer.                                                                                                                         |
|`int`        |`BATTERY_PROPERTY_ENERGY_COUNTER`<br><br>Battery remaining energy in nanowatt-hours, as a long integer.                                                                                                                     |
|`int`        |`BATTERY_PROPERTY_STATUS`<br><br>Battery charge status, from a BATTERY\_STATUS\_\* value.                                                                                                                                   |
|`int`        |`BATTERY_STATUS_CHARGING`<br><br><br/>                                                                                                                                                                                      |
|`int`        |`BATTERY_STATUS_DISCHARGING`<br><br><br/>                                                                                                                                                                                   |
|`int`        |`BATTERY_STATUS_FULL`<br><br><br/>                                                                                                                                                                                          |
|`int`        |`BATTERY_STATUS_NOT_CHARGING`<br><br><br/>                                                                                                                                                                                  |
|`int`        |`BATTERY_STATUS_UNKNOWN`<br><br><br/>                                                                                                                                                                                       |
|`String`     |`EXTRA_BATTERY_LOW`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: Boolean field indicating whether the battery is currently considered to be low, that is whether a `Intent#ACTION_BATTERY_LOW` broadcast has been sent.|
|`String`     |`EXTRA_CHARGING_STATUS`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: Int value representing the battery charging status.                                                                                               |
|`String`     |`EXTRA_CYCLE_COUNT`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: Int value representing the battery charging cycle count.                                                                                              |
|`String`     |`EXTRA_HEALTH`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: integer containing the current health constant.                                                                                                            |
|`String`     |`EXTRA_ICON_SMALL`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: integer containing the resource ID of a small status bar icon indicating the current battery state.                                                    |
|`String`     |`EXTRA_LEVEL`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: integer field containing the current battery level, from 0 to `EXTRA_SCALE`.                                                                                |
|`String`     |`EXTRA_PLUGGED`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: integer indicating whether the device is plugged in to a power source; 0 means it is on battery, other constants are different types of power sources.    |
|`String`     |`EXTRA_PRESENT`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: boolean indicating whether a battery is present.                                                                                                          |
|`String`     |`EXTRA_SCALE`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: integer containing the maximum battery level.                                                                                                               |
|`String`     |`EXTRA_STATUS`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: integer containing the current status constant.                                                                                                            |
|`String`     |`EXTRA_TECHNOLOGY`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: String describing the technology of the current battery.                                                                                               |
|`String`     |`EXTRA_TEMPERATURE`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: integer containing the current battery temperature.                                                                                                   |
|`String`     |`EXTRA_VOLTAGE`<br><br>Extra for `Intent.ACTION_BATTERY_CHANGED`: integer containing the current battery voltage level.                                                                                                     |

<br/>

<br/>

<br/>

|### Public methods|                                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`long`            |`computeChargeTimeRemaining()`<br><br>Compute an approximation for how much time (in milliseconds) remains until the battery is fully charged.                                 |
|`int`             |`getIntProperty(int id)`<br><br>Return the value of a battery property of integer type.                                                                                        |
|`long`            |`getLongProperty(int id)`<br><br>Return the value of a battery property of long type If the platform does not provide the property queried, this value will be Long.MIN\_VALUE.|
|`boolean`         |`isCharging()`<br><br>Return true if the battery is currently considered to be charging.                                                                                       |

<br/>

## Constants

### ACTION\_CHARGING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String ACTION_CHARGING
```

Sent when the device's battery has started charging (or has reached full charge and the device is on power). This is a good time to do work that you would like to avoid doing while on battery (that is to avoid draining the user's battery due to things they don't care enough about). This is paired with `ACTION_DISCHARGING`. The current state can always be retrieved with `isCharging()`.

<br/>

Constant Value: "android.os.action.CHARGING"

### ACTION\_DISCHARGING

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String ACTION_DISCHARGING
```

Sent when the device's battery may be discharging, so apps should avoid doing extraneous work that would cause it to discharge faster. This is paired with `ACTION_CHARGING`. The current state can always be retrieved with `isCharging()`.

<br/>

Constant Value: "android.os.action.DISCHARGING"

### BATTERY\_HEALTH\_COLD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_HEALTH_COLD
```

<br/>

<br/>

Constant Value: 7 (0x00000007)

### BATTERY\_HEALTH\_DEAD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_HEALTH_DEAD
```

<br/>

<br/>

Constant Value: 4 (0x00000004)

### BATTERY\_HEALTH\_GOOD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_HEALTH_GOOD
```

<br/>

<br/>

Constant Value: 2 (0x00000002)

### BATTERY\_HEALTH\_OVERHEAT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_HEALTH_OVERHEAT
```

<br/>

<br/>

Constant Value: 3 (0x00000003)

### BATTERY\_HEALTH\_OVER\_VOLTAGE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_HEALTH_OVER_VOLTAGE
```

<br/>

<br/>

Constant Value: 5 (0x00000005)

### BATTERY\_HEALTH\_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_HEALTH_UNKNOWN
```

<br/>

<br/>

Constant Value: 1 (0x00000001)

### BATTERY\_HEALTH\_UNSPECIFIED\_FAILURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_HEALTH_UNSPECIFIED_FAILURE
```

<br/>

<br/>

Constant Value: 6 (0x00000006)

### BATTERY\_PLUGGED\_AC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_PLUGGED_AC
```

Power source is an AC charger.

<br/>

Constant Value: 1 (0x00000001)

### BATTERY\_PLUGGED\_DOCK

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_PLUGGED_DOCK
```

Power source is dock.

<br/>

Constant Value: 8 (0x00000008)

### BATTERY\_PLUGGED\_USB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_PLUGGED_USB
```

Power source is a USB port.

<br/>

Constant Value: 2 (0x00000002)

### BATTERY\_PLUGGED\_WIRELESS

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_PLUGGED_WIRELESS
```

Power source is wireless.

<br/>

Constant Value: 4 (0x00000004)

### BATTERY\_PROPERTY\_CAPACITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_PROPERTY_CAPACITY
```

Remaining battery capacity as an integer percentage of total capacity (with no fractional part).

<br/>

Constant Value: 4 (0x00000004)

### BATTERY\_PROPERTY\_CHARGE\_COUNTER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_PROPERTY_CHARGE_COUNTER
```

Battery capacity in microampere-hours, as an integer.

<br/>

Constant Value: 1 (0x00000001)

### BATTERY\_PROPERTY\_CURRENT\_AVERAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_PROPERTY_CURRENT_AVERAGE
```

Average battery current in microamperes, as an integer. Positive values indicate net current entering the battery from a charge source, negative values indicate net current discharging from the battery. The time period over which the average is computed may depend on the fuel gauge hardware and its configuration.

<br/>

Constant Value: 3 (0x00000003)

### BATTERY\_PROPERTY\_CURRENT\_NOW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_PROPERTY_CURRENT_NOW
```

Instantaneous battery current in microamperes, as an integer. Positive values indicate net current entering the battery from a charge source, negative values indicate net current discharging from the battery.

<br/>

Constant Value: 2 (0x00000002)

### BATTERY\_PROPERTY\_ENERGY\_COUNTER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_PROPERTY_ENERGY_COUNTER
```

Battery remaining energy in nanowatt-hours, as a long integer.

<br/>

Constant Value: 5 (0x00000005)

### BATTERY\_PROPERTY\_STATUS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_PROPERTY_STATUS
```

Battery charge status, from a BATTERY\_STATUS\_\* value.

<br/>

Constant Value: 6 (0x00000006)

### BATTERY\_STATUS\_CHARGING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_STATUS_CHARGING
```

<br/>

<br/>

Constant Value: 2 (0x00000002)

### BATTERY\_STATUS\_DISCHARGING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_STATUS_DISCHARGING
```

<br/>

<br/>

Constant Value: 3 (0x00000003)

### BATTERY\_STATUS\_FULL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_STATUS_FULL
```

<br/>

<br/>

Constant Value: 5 (0x00000005)

### BATTERY\_STATUS\_NOT\_CHARGING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_STATUS_NOT_CHARGING
```

<br/>

<br/>

Constant Value: 4 (0x00000004)

### BATTERY\_STATUS\_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int BATTERY_STATUS_UNKNOWN
```

<br/>

<br/>

Constant Value: 1 (0x00000001)

### EXTRA\_BATTERY\_LOW

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_BATTERY_LOW
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: Boolean field indicating whether the battery is currently considered to be low, that is whether a `Intent#ACTION_BATTERY_LOW` broadcast has been sent.

<br/>

Constant Value: "battery\_low"

### EXTRA\_CHARGING\_STATUS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_CHARGING_STATUS
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: Int value representing the battery charging status.

<br/>

Constant Value: "android.os.extra.CHARGING\_STATUS"

### EXTRA\_CYCLE\_COUNT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_CYCLE_COUNT
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: Int value representing the battery charging cycle count.

<br/>

Constant Value: "android.os.extra.CYCLE\_COUNT"

### EXTRA\_HEALTH

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_HEALTH
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: integer containing the current health constant.

<br/>

Constant Value: "health"

### EXTRA\_ICON\_SMALL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_ICON_SMALL
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: integer containing the resource ID of a small status bar icon indicating the current battery state.

<br/>

Constant Value: "icon-small"

### EXTRA\_LEVEL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_LEVEL
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: integer field containing the current battery level, from 0 to `EXTRA_SCALE`.

<br/>

Constant Value: "level"

### EXTRA\_PLUGGED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_PLUGGED
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: integer indicating whether the device is plugged in to a power source; 0 means it is on battery, other constants are different types of power sources.

<br/>

Constant Value: "plugged"

### EXTRA\_PRESENT

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_PRESENT
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: boolean indicating whether a battery is present.

<br/>

Constant Value: "present"

### EXTRA\_SCALE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_SCALE
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: integer containing the maximum battery level.

<br/>

Constant Value: "scale"

### EXTRA\_STATUS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_STATUS
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: integer containing the current status constant.

<br/>

Constant Value: "status"

### EXTRA\_TECHNOLOGY

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_TECHNOLOGY
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: String describing the technology of the current battery.

<br/>

Constant Value: "technology"

### EXTRA\_TEMPERATURE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_TEMPERATURE
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: integer containing the current battery temperature.

<br/>

Constant Value: "temperature"

### EXTRA\_VOLTAGE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String EXTRA_VOLTAGE
```

Extra for `Intent.ACTION_BATTERY_CHANGED`: integer containing the current battery voltage level.

<br/>

Constant Value: "voltage"

## Public methods

### computeChargeTimeRemaining

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public long computeChargeTimeRemaining ()
```

Compute an approximation for how much time (in milliseconds) remains until the battery is fully charged. Returns -1 if no time can be computed: either there is not enough current data to make a decision or the battery is currently discharging.

<br/>

<br/>

|Returns|                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------|
|`long` |how much time is left, in milliseconds, until the battery is fully charged or -1 if the computation fails<br><br><br/>|

<br/>

### getIntProperty

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public int getIntProperty (int id)
```

Return the value of a battery property of integer type.

<br/>

<br/>

|Parameters|                                                        |
|----------|--------------------------------------------------------|
|`id`      |`int`: identifier of the requested property<br><br><br/>|

<br/>

|Returns|                                                                                                                                                                                                                       |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`int`  |the property value. If the property is not supported or there is any other error, return (a) 0 if `targetSdkVersion < VERSION_CODES.P` or (b) Integer.MIN\_VALUE if `targetSdkVersion >= VERSION_CODES.P`.<br><br><br/>|

<br/>

### getLongProperty

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public long getLongProperty (int id)
```

Return the value of a battery property of long type If the platform does not provide the property queried, this value will be Long.MIN\_VALUE.

<br/>

<br/>

|Parameters|                                                        |
|----------|--------------------------------------------------------|
|`id`      |`int`: identifier of the requested property<br><br><br/>|

<br/>

|Returns|                                                                     |
|-------|---------------------------------------------------------------------|
|`long` |the property value, or Long.MIN\_VALUE if not supported.<br><br><br/>|

<br/>

### isCharging

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public boolean isCharging ()
```

Return true if the battery is currently considered to be charging. This means that the device is plugged in and is supplying sufficient power that the battery level is going up (or the battery is fully charged). Changes in this state are matched by broadcasts of `ACTION_CHARGING` and `ACTION_DISCHARGING`.

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBQW5kcm9pZEFzeW5jJTNBJTNBdXNlcnRlc3Rpbmctc3dpbW0=/docs/o0aa1koc).
