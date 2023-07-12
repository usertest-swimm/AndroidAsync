---
id: 38sbho0w
title: Base Bundle
file_version: 1.1.3
app_version: 1.12.1
---

A mapping from String keys to values of various types. In most cases, you should work directly with either the `Bundle` or `PersistableBundle` subclass.

## Summary

<br/>

|### Public methods|                                                                                                                                                                                                                                               |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`void`            |`clear()`<br><br>Removes all elements from the mapping of this Bundle.                                                                                                                                                                         |
|`boolean`         |`containsKey(String key)`<br><br>Returns true if the given key is contained in the mapping of this Bundle.                                                                                                                                     |
|`Object`          |`get(String key)`<br><br>_This method was deprecated in API level 33. Use the type-safe specific APIs depending on the type of the item to be retrieved, eg._ `getString(java.lang.String)`.                                                   |
|`boolean`         |`getBoolean(String key, boolean defaultValue)`<br><br>Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.                                                             |
|`boolean`         |`getBoolean(String key)`<br><br>Returns the value associated with the given key, or false if no mapping of the desired type exists for the given key.                                                                                          |
|`boolean[]`       |`getBooleanArray(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                |
|`double`          |`getDouble(String key, double defaultValue)`<br><br>Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.                                                               |
|`double`          |`getDouble(String key)`<br><br>Returns the value associated with the given key, or 0.0 if no mapping of the desired type exists for the given key.                                                                                             |
|`double[]`        |`getDoubleArray(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                 |
|`int`             |`getInt(String key)`<br><br>Returns the value associated with the given key, or 0 if no mapping of the desired type exists for the given key.                                                                                                  |
|`int`             |`getInt(String key, int defaultValue)`<br><br>Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.                                                                     |
|`int[]`           |`getIntArray(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                    |
|`long`            |`getLong(String key)`<br><br>Returns the value associated with the given key, or 0L if no mapping of the desired type exists for the given key.                                                                                                |
|`long`            |`getLong(String key, long defaultValue)`<br><br>Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.                                                                   |
|`long[]`          |`getLongArray(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                   |
|`String`          |`getString(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                      |
|`String`          |`getString(String key, String defaultValue)`<br><br>Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key or if a null value is explicitly associated with the given key.|
|`String[]`        |`getStringArray(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                 |
|`boolean`         |`isEmpty()`<br><br>Returns true if the mapping of this Bundle is empty, false otherwise.                                                                                                                                                       |
|`Set<String>`     |`keySet()`<br><br>Returns a Set containing the Strings used as keys in this Bundle.                                                                                                                                                            |
|`void`            |`putAll(PersistableBundle bundle)`<br><br>Inserts all mappings from the given PersistableBundle into this BaseBundle.                                                                                                                          |
|`void`            |`putBoolean(String key, boolean value)`<br><br>Inserts a Boolean value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                        |
|`void`            |`putBooleanArray(String key, boolean[] value)`<br><br>Inserts a boolean array value into the mapping of this Bundle, replacing any existing value for the given key.                                                                           |
|`void`            |`putDouble(String key, double value)`<br><br>Inserts a double value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                           |
|`void`            |`putDoubleArray(String key, double[] value)`<br><br>Inserts a double array value into the mapping of this Bundle, replacing any existing value for the given key.                                                                              |
|`void`            |`putInt(String key, int value)`<br><br>Inserts an int value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                                   |
|`void`            |`putIntArray(String key, int[] value)`<br><br>Inserts an int array value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                      |
|`void`            |`putLong(String key, long value)`<br><br>Inserts a long value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                                 |
|`void`            |`putLongArray(String key, long[] value)`<br><br>Inserts a long array value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                    |
|`void`            |`putString(String key, String value)`<br><br>Inserts a String value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                           |
|`void`            |`putStringArray(String key, String[] value)`<br><br>Inserts a String array value into the mapping of this Bundle, replacing any existing value for the given key.                                                                              |
|`void`            |`remove(String key)`<br><br>Removes any entry with the given key from the mapping of this Bundle.                                                                                                                                              |
|`int`             |`size()`<br><br>Returns the number of mappings contained in this Bundle.                                                                                                                                                                       |

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBQW5kcm9pZEFzeW5jJTNBJTNBdXNlcnRlc3Rpbmctc3dpbW0=/docs/38sbho0w).
