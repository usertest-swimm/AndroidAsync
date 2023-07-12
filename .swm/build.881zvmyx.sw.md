---
id: 881zvmyx
title: Build
file_version: 1.1.3
app_version: 1.12.1
---

## Summary

<br/>

|### Nested classes|                                                                                  |
|------------------|----------------------------------------------------------------------------------|
|`class`           |`Build.Partition`<br><br>Build information for a particular device partition.     |
|`class`           |`Build.VERSION`<br><br>Various version strings.                                   |
|`class`           |`Build.VERSION_CODES`<br><br>Enumeration of the currently known SDK version codes.|

<br/>

|### Constants|                                                                 |
|-------------|-----------------------------------------------------------------|
|`String`     |`UNKNOWN`<br><br>Value used for when a build property is unknown.|

<br/>

|### Fields                    |                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`public static final String`  |`BOARD`<br><br>The name of the underlying board, like "goldfish".                                                                                                                                                                         |
|`public static final String`  |`BOOTLOADER`<br><br>The system bootloader version number.                                                                                                                                                                                 |
|`public static final String`  |`BRAND`<br><br>The consumer-visible brand with which the product/hardware will be associated, if any.                                                                                                                                     |
|`public static final String`  |`CPU_ABI`<br><br>_This field was deprecated in API level 21. Use_ `SUPPORTED_ABIS` instead.                                                                                                                                               |
|`public static final String`  |`CPU_ABI2`<br><br>_This field was deprecated in API level 21. Use_ `SUPPORTED_ABIS` instead.                                                                                                                                              |
|`public static final String`  |`DEVICE`<br><br>The name of the industrial design.                                                                                                                                                                                        |
|`public static final String`  |`DISPLAY`<br><br>A build ID string meant for displaying to the user                                                                                                                                                                       |
|`public static final String`  |`FINGERPRINT`<br><br>A string that uniquely identifies this build.                                                                                                                                                                        |
|`public static final String`  |`HARDWARE`<br><br>The name of the hardware (from the kernel command line or /proc).                                                                                                                                                       |
|`public static final String`  |`HOST`<br><br><br/>                                                                                                                                                                                                                       |
|`public static final String`  |`ID`<br><br>Either a changelist number, or a label like "M4-rc20".                                                                                                                                                                        |
|`public static final String`  |`MANUFACTURER`<br><br>The manufacturer of the product/hardware.                                                                                                                                                                           |
|`public static final String`  |`MODEL`<br><br>The end-user-visible name for the end product.                                                                                                                                                                             |
|`public static final String`  |`ODM_SKU`<br><br>The SKU of the device as set by the original design manufacturer (ODM).                                                                                                                                                  |
|`public static final String`  |`PRODUCT`<br><br>The name of the overall product.                                                                                                                                                                                         |
|`public static final String`  |`RADIO`<br><br>_This field was deprecated in API level 15. The radio firmware version is frequently not available when this class is initialized, leading to a blank or "unknown" value for this string. Use_ `getRadioVersion()` instead.|
|`public static final String`  |`SERIAL`<br><br>_This field was deprecated in API level 26. Use_ `getSerial()` instead.                                                                                                                                                   |
|`public static final String`  |`SKU`<br><br>The SKU of the hardware (from the kernel command line).                                                                                                                                                                      |
|`public static final String`  |`SOC_MANUFACTURER`<br><br>The manufacturer of the device's primary system-on-chip.                                                                                                                                                        |
|`public static final String`  |`SOC_MODEL`<br><br>The model name of the device's primary system-on-chip.                                                                                                                                                                 |
|`public static final String[]`|`SUPPORTED_32_BIT_ABIS`<br><br>An ordered list of **32 bit** ABIs supported by this device.                                                                                                                                               |
|`public static final String[]`|`SUPPORTED_64_BIT_ABIS`<br><br>An ordered list of **64 bit** ABIs supported by this device.                                                                                                                                               |
|`public static final String[]`|`SUPPORTED_ABIS`<br><br>An ordered list of ABIs supported by this device.                                                                                                                                                                 |
|`public static final String`  |`TAGS`<br><br>Comma-separated tags describing the build, like "unsigned,debug".                                                                                                                                                           |
|`public static final long`    |`TIME`<br><br>The time at which the build was produced, given in milliseconds since the UNIX epoch.                                                                                                                                       |
|`public static final String`  |`TYPE`<br><br>The type of build, like "user" or "eng".                                                                                                                                                                                    |
|`public static final String`  |`USER`<br><br><br/>                                                                                                                                                                                                                       |

<br/>

|### Public constructors|     |
|-----------------------|-----|
|`Build()`              |<br/>|

<br/>

|### Public methods            |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
|`static List<Build.Partition>`|`getFingerprintedPartitions()`<br><br>Get build information about partitions that have a separate fingerprint defined.|
|`static String`               |`getRadioVersion()`<br><br>Returns the version string for the radio firmware.                                         |
|`static String`               |`getSerial()`<br><br>Gets the hardware serial number, if available.                                                   |

<br/>

|<br/>                        |### Inherited methods|
|-----------------------------|---------------------|
|From class `java.lang.Object`|                     |

<br/>

## Constants

### UNKNOWN

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String UNKNOWN
```

Value used for when a build property is unknown.

<br/>

Constant Value: "unknown"

## Fields

### BOARD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String BOARD
```

The name of the underlying board, like "goldfish".

<br/>

### BOOTLOADER

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String BOOTLOADER
```

The system bootloader version number.

<br/>

### BRAND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String BRAND
```

The consumer-visible brand with which the product/hardware will be associated, if any.

<br/>

### CPU\_ABI

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)<br/>
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String CPU_ABI
```

<br/>

**This field was deprecated in API level 21.**<br/>
Use `SUPPORTED_ABIS` instead.

The name of the instruction set (CPU type + ABI convention) of native code.

<br/>

### CPU\_ABI2

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)<br/>
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String CPU_ABI2
```

<br/>

**This field was deprecated in API level 21.**<br/>
Use `SUPPORTED_ABIS` instead.

The name of the second instruction set (CPU type + ABI convention) of native code.

<br/>

### DEVICE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String DEVICE
```

The name of the industrial design.

<br/>

### DISPLAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String DISPLAY
```

A build ID string meant for displaying to the user

<br/>

### FINGERPRINT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String FINGERPRINT
```

A string that uniquely identifies this build. Do not attempt to parse this value.

<br/>

### HARDWARE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String HARDWARE
```

The name of the hardware (from the kernel command line or /proc).

<br/>

### HOST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String HOST
```

<br/>

<br/>

### ID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String ID
```

Either a changelist number, or a label like "M4-rc20".

<br/>

### MANUFACTURER

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String MANUFACTURER
```

The manufacturer of the product/hardware.

<br/>

### MODEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String MODEL
```

The end-user-visible name for the end product.

<br/>

### ODM\_SKU

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String ODM_SKU
```

The SKU of the device as set by the original design manufacturer (ODM).

This is a runtime-initialized property set during startup to configure device services. If no value is set, this is reported as `UNKNOWN`.

The ODM SKU may have multiple variants for the same system SKU in case a manufacturer produces variants of the same design. For example, the same build may be released with variations in physical keyboard and/or display hardware, each with a different ODM SKU.

<br/>

### PRODUCT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String PRODUCT
```

The name of the overall product.

<br/>

### RADIO

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)<br/>
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String RADIO
```

<br/>

**This field was deprecated in API level 15.**<br/>
The radio firmware version is frequently not available when this class is initialized, leading to a blank or "unknown" value for this string. Use `getRadioVersion()` instead.

The radio firmware version number.

<br/>

### SERIAL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)<br/>
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String SERIAL
```

<br/>

**This field was deprecated in API level 26.**<br/>
Use `getSerial()` instead.

A hardware serial number, if available. Alphanumeric only, case-insensitive. This field is always set to `Build#UNKNOWN`.

<br/>

### SKU

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String SKU
```

The SKU of the hardware (from the kernel command line).

The SKU is reported by the bootloader to configure system software features. If no value is supplied by the bootloader, this is reported as `UNKNOWN`.

<br/>

### SOC\_MANUFACTURER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String SOC_MANUFACTURER
```

The manufacturer of the device's primary system-on-chip.

<br/>

### SOC\_MODEL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String SOC_MODEL
```

The model name of the device's primary system-on-chip.

<br/>

### SUPPORTED\_32\_BIT\_ABIS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String[] SUPPORTED_32_BIT_ABIS
```

An ordered list of **32 bit** ABIs supported by this device. The most preferred ABI is the first element in the list. See `SUPPORTED_ABIS` and `SUPPORTED_64_BIT_ABIS`.

<br/>

### SUPPORTED\_64\_BIT\_ABIS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String[] SUPPORTED_64_BIT_ABIS
```

An ordered list of **64 bit** ABIs supported by this device. The most preferred ABI is the first element in the list. See `SUPPORTED_ABIS` and `SUPPORTED_32_BIT_ABIS`.

<br/>

### SUPPORTED\_ABIS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String[] SUPPORTED_ABIS
```

An ordered list of ABIs supported by this device. The most preferred ABI is the first element in the list. See `SUPPORTED_32_BIT_ABIS` and `SUPPORTED_64_BIT_ABIS`.

<br/>

### TAGS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String TAGS
```

Comma-separated tags describing the build, like "unsigned,debug".

<br/>

### TIME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final long TIME
```

The time at which the build was produced, given in milliseconds since the UNIX epoch.

<br/>

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String TYPE
```

The type of build, like "user" or "eng".

<br/>

### USER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final String USER
```

<br/>

<br/>

## Public constructors

### Build

```
public Build ()
```

<br/>

<br/>

## Public methods

### getFingerprintedPartitions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static List<Build.Partition> getFingerprintedPartitions ()
```

Get build information about partitions that have a separate fingerprint defined. The list includes partitions that are suitable candidates for over-the-air updates. This is not an exhaustive list of partitions on the device.

<br/>

<br/>

|Returns                |                                         |
|-----------------------|-----------------------------------------|
|`List<Build.Partition>`|This value cannot be `null`.<br><br><br/>|

<br/>

### getRadioVersion

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static String getRadioVersion ()
```

Returns the version string for the radio firmware. May return null (if, for instance, the radio is not currently on).

<br/>

<br/>

|Returns |     |
|--------|-----|
|`String`|<br/>|

<br/>

### getSerial

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static String getSerial ()
```

Gets the hardware serial number, if available.

**Note:** Root access may allow you to modify device identifiers, such as the hardware serial number. If you change these identifiers, you can not use [key attestation](https://developer.android.com/training/articles/security-key-attestation) to obtain proof of the device's original identifiers. KeyMint will reject an ID attestation request if the identifiers provided by the frameworks do not match the identifiers it was provisioned with.

Starting with API level 29, persistent device identifiers are guarded behind additional restrictions, and apps are recommended to use resettable identifiers (see [Best practices for unique identifiers](https://developer.android.com/training/articles/user-data-ids)). This method can be invoked if one of the following requirements is met:

*   If the calling app has been granted the READ\_PRIVILEGED\_PHONE\_STATE permission; this is a privileged permission that can only be granted to apps preloaded on the device.

*   If the calling app has carrier privileges (see `TelephonyManager.hasCarrierPrivileges()`) on any active subscription.

*   If the calling app is the default SMS role holder (see `RoleManager.isRoleHeld(String)`).

*   If the calling app is the device owner of a fully-managed device, a profile owner of an organization-owned device, or their delegates (see `DevicePolicyManager.getEnrollmentSpecificId()`).

If the calling app does not meet one of these requirements then this method will behave as follows:

*   If the calling app's target SDK is API level 28 or lower and the app has the READ\_PHONE\_STATE permission then `Build#UNKNOWN` is returned.

*   If the calling app's target SDK is API level 28 or lower and the app does not have the READ\_PHONE\_STATE permission, or if the calling app is targeting API level 29 or higher, then a SecurityException is thrown.

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBQW5kcm9pZEFzeW5jJTNBJTNBdXNlcnRlc3Rpbmctc3dpbW0=/docs/881zvmyx).
