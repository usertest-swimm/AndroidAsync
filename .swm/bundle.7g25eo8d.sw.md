---
id: 7g25eo8d
title: Bundle
file_version: 1.1.3
app_version: 1.12.1
---

A mapping from String keys to various `Parcelable` values.

**Warning:** Note that `Bundle` is a lazy container and as such it does NOT implement `Object.equals(java.lang.Object)` or `Object.hashCode()`.

**See also:**

*   `PersistableBundle`

## Summary

<br/>

|### Inherited constants               |
|--------------------------------------|
|From interface `android.os.Parcelable`|

<br/>

|### Fields                           |                                                               |
|-------------------------------------|---------------------------------------------------------------|
|`public static final Creator<Bundle>`|`CREATOR`<br><br><br/>                                         |
|`public static final Bundle`         |`EMPTY`<br><br>An unmodifiable `Bundle` that is always `empty`.|

<br/>

|### Public constructors                                                                                                                                   |     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
|`Bundle()`<br><br>Constructs a new, empty Bundle.                                                                                                         |<br/>|
|`Bundle(ClassLoader loader)`<br><br>Constructs a new, empty Bundle that uses a specific ClassLoader for instantiating Parcelable and Serializable objects.|<br/>|
|`Bundle(int capacity)`<br><br>Constructs a new, empty Bundle sized to hold the given number of elements.                                                  |<br/>|
|`Bundle(Bundle b)`<br><br>Constructs a Bundle containing a copy of the mappings from the given Bundle.                                                    |<br/>|
|`Bundle(PersistableBundle b)`<br><br>Constructs a Bundle containing a copy of the mappings from the given PersistableBundle.                              |<br/>|

<br/>

|### Public methods                     |                                                                                                                                                                                                                                                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`void`                                 |`clear()`<br><br>Removes all elements from the mapping of this Bundle.                                                                                                                                                                                    |
|`Object`                               |`clone()`<br><br>Clones the current Bundle.                                                                                                                                                                                                               |
|`Bundle`                               |`deepCopy()`<br><br>Make a deep copy of the given bundle.                                                                                                                                                                                                 |
|`int`                                  |`describeContents()`<br><br>Report the nature of this Parcelable's contents                                                                                                                                                                               |
|`IBinder`                              |`getBinder(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                                 |
|`Bundle`                               |`getBundle(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                                 |
|`byte`                                 |`getByte(String key)`<br><br>Returns the value associated with the given key, or (byte) 0 if no mapping of the desired type exists for the given key.                                                                                                     |
|`Byte`                                 |`getByte(String key, byte defaultValue)`<br><br>Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.                                                                              |
|`byte[]`                               |`getByteArray(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                              |
|`char`                                 |`getChar(String key)`<br><br>Returns the value associated with the given key, or (char) 0 if no mapping of the desired type exists for the given key.                                                                                                     |
|`char`                                 |`getChar(String key, char defaultValue)`<br><br>Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.                                                                              |
|`char[]`                               |`getCharArray(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                              |
|`CharSequence`                         |`getCharSequence(String key, CharSequence defaultValue)`<br><br>Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key or if a null value is explicitly associatd with the given key.|
|`CharSequence`                         |`getCharSequence(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                           |
|`CharSequence[]`                       |`getCharSequenceArray(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                      |
|`ArrayList<CharSequence>`              |`getCharSequenceArrayList(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                  |
|`ClassLoader`                          |`getClassLoader()`<br><br>Return the ClassLoader currently associated with this Bundle.                                                                                                                                                                   |
|`float`                                |`getFloat(String key, float defaultValue)`<br><br>Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.                                                                            |
|`float`                                |`getFloat(String key)`<br><br>Returns the value associated with the given key, or 0.0f if no mapping of the desired type exists for the given key.                                                                                                        |
|`float[]`                              |`getFloatArray(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                             |
|`ArrayList<Integer>`                   |`getIntegerArrayList(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                       |
|`<T extends Parcelable> T`             |`getParcelable(String key)`<br><br>_This method was deprecated in API level 33. Use the type-safer_ `getParcelable(java.lang.String, java.lang.Class)` starting from Android `Build.VERSION_CODES#TIRAMISU`.                                              |
|`<T> T`                                |`getParcelable(String key, Class<T> clazz)`<br><br>Returns the value associated with the given key or `null` if:<br><br>*   No mapping of the desired type exists for the given key.<br><br>    <br/>                                                     |
|`<T> T[]`                              |`getParcelableArray(String key, Class<T> clazz)`<br><br>Returns the value associated with the given key, or `null` if:<br><br>*   No mapping of the desired type exists for the given key.<br><br>    <br/>                                               |
|`Parcelable[]`                         |`getParcelableArray(String key)`<br><br>_This method was deprecated in API level 33. Use the type-safer_ `getParcelableArray(java.lang.String, java.lang.Class)` starting from Android `Build.VERSION_CODES#TIRAMISU`.                                    |
|`<T> ArrayList<T>`                     |`getParcelableArrayList(String key, Class<? extends T> clazz)`<br><br>Returns the value associated with the given key, or `null` if:<br><br>*   No mapping of the desired type exists for the given key.<br><br>    <br/>                                 |
|`<T extends Parcelable> ArrayList<T>`  |`getParcelableArrayList(String key)`<br><br>_This method was deprecated in API level 33. Use the type-safer_ `getParcelable(java.lang.String, java.lang.Class)` starting from Android `Build.VERSION_CODES#TIRAMISU`.                                     |
|`<T extends Serializable> T`           |`getSerializable(String key, Class<T> clazz)`<br><br>Returns the value associated with the given key, or `null` if:<br><br>*   No mapping of the desired type exists for the given key.<br><br>    <br/>                                                  |
|`Serializable`                         |`getSerializable(String key)`<br><br>_This method was deprecated in API level 33. Use the type-safer_ `getSerializable(java.lang.String, java.lang.Class)` starting from Android `Build.VERSION_CODES#TIRAMISU`.                                          |
|`short`                                |`getShort(String key)`<br><br>Returns the value associated with the given key, or (short) 0 if no mapping of the desired type exists for the given key.                                                                                                   |
|`short`                                |`getShort(String key, short defaultValue)`<br><br>Returns the value associated with the given key, or defaultValue if no mapping of the desired type exists for the given key.                                                                            |
|`short[]`                              |`getShortArray(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                             |
|`Size`                                 |`getSize(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                                   |
|`SizeF`                                |`getSizeF(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                                  |
|`<T extends Parcelable> SparseArray<T>`|`getSparseParcelableArray(String key)`<br><br>_This method was deprecated in API level 33. Use the type-safer_ `getSparseParcelableArray(java.lang.String, java.lang.Class)` starting from Android `Build.VERSION_CODES#TIRAMISU`.                        |
|`<T> SparseArray<T>`                   |`getSparseParcelableArray(String key, Class<? extends T> clazz)`<br><br>Returns the value associated with the given key, or `null` if:<br><br>*   No mapping of the desired type exists for the given key.<br><br>    <br/>                               |
|`ArrayList<String>`                    |`getStringArrayList(String key)`<br><br>Returns the value associated with the given key, or null if no mapping of the desired type exists for the given key or a null value is explicitly associated with the key.                                        |
|`boolean`                              |`hasFileDescriptors()`<br><br>Reports whether the bundle contains any parcelled file descriptors.                                                                                                                                                         |
|`void`                                 |`putAll(Bundle bundle)`<br><br>Inserts all mappings from the given Bundle into this Bundle.                                                                                                                                                               |
|`void`                                 |`putBinder(String key, IBinder value)`<br><br>Inserts an `IBinder` value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                                 |
|`void`                                 |`putBundle(String key, Bundle value)`<br><br>Inserts a Bundle value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                                      |
|`void`                                 |`putByte(String key, byte value)`<br><br>Inserts a byte value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                                            |
|`void`                                 |`putByteArray(String key, byte[] value)`<br><br>Inserts a byte array value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                               |
|`void`                                 |`putChar(String key, char value)`<br><br>Inserts a char value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                                            |
|`void`                                 |`putCharArray(String key, char[] value)`<br><br>Inserts a char array value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                               |
|`void`                                 |`putCharSequence(String key, CharSequence value)`<br><br>Inserts a CharSequence value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                    |
|`void`                                 |`putCharSequenceArray(String key, CharSequence[] value)`<br><br>Inserts a CharSequence array value into the mapping of this Bundle, replacing any existing value for the given key.                                                                       |
|`void`                                 |`putCharSequenceArrayList(String key, ArrayList<CharSequence> value)`<br><br>Inserts an ArrayList value into the mapping of this Bundle, replacing any existing value for the given key.                                                                  |
|`void`                                 |`putFloat(String key, float value)`<br><br>Inserts a float value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                                         |
|`void`                                 |`putFloatArray(String key, float[] value)`<br><br>Inserts a float array value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                            |
|`void`                                 |`putIntegerArrayList(String key, ArrayList<Integer> value)`<br><br>Inserts an ArrayList value into the mapping of this Bundle, replacing any existing value for the given key.                                                                            |
|`void`                                 |`putParcelable(String key, Parcelable value)`<br><br>Inserts a Parcelable value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                          |
|`void`                                 |`putParcelableArray(String key, Parcelable[] value)`<br><br>Inserts an array of Parcelable values into the mapping of this Bundle, replacing any existing value for the given key.                                                                        |
|`void`                                 |`putParcelableArrayList(String key, ArrayList<? extends Parcelable> value)`<br><br>Inserts a List of Parcelable values into the mapping of this Bundle, replacing any existing value for the given key.                                                   |
|`void`                                 |`putSerializable(String key, Serializable value)`<br><br>Inserts a Serializable value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                    |
|`void`                                 |`putShort(String key, short value)`<br><br>Inserts a short value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                                         |
|`void`                                 |`putShortArray(String key, short[] value)`<br><br>Inserts a short array value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                            |
|`void`                                 |`putSize(String key, Size value)`<br><br>Inserts a Size value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                                            |
|`void`                                 |`putSizeF(String key, SizeF value)`<br><br>Inserts a SizeF value into the mapping of this Bundle, replacing any existing value for the given key.                                                                                                         |
|`void`                                 |`putSparseParcelableArray(String key, SparseArray<? extends Parcelable> value)`<br><br>Inserts a SparceArray of Parcelable values into the mapping of this Bundle, replacing any existing value for the given key.                                        |
|`void`                                 |`putStringArrayList(String key, ArrayList<String> value)`<br><br>Inserts an ArrayList value into the mapping of this Bundle, replacing any existing value for the given key.                                                                              |
|`void`                                 |`readFromParcel(Parcel parcel)`<br><br>Reads the Parcel contents into this Bundle, typically in order for it to be passed through an IBinder connection.                                                                                                  |
|`void`                                 |`remove(String key)`<br><br>Removes any entry with the given key from the mapping of this Bundle.                                                                                                                                                         |
|`void`                                 |`setClassLoader(ClassLoader loader)`<br><br>Changes the ClassLoader this Bundle uses when instantiating objects.                                                                                                                                          |
|`String`                               |`toString()`<br><br>Returns a string representation of the `Bundle` that may be suitable for debugging.                                                                                                                                                   |
|`void`                                 |`writeToParcel(Parcel parcel, int flags)`<br><br>Writes the Bundle contents to a Parcel, typically in order for it to be passed through an IBinder connection.                                                                                            |

<br/>

|<br/>                                 |### Inherited methods|
|--------------------------------------|---------------------|
|From class `android.os.BaseBundle`    |                     |
|From class `java.lang.Object`         |                     |
|From interface `android.os.Parcelable`|                     |

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBQW5kcm9pZEFzeW5jJTNBJTNBdXNlcnRlc3Rpbmctc3dpbW0=/docs/7g25eo8d).
