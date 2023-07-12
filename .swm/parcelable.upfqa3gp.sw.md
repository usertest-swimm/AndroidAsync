---
id: upfqa3gp
title: Parcelable
file_version: 1.1.3
app_version: 1.12.1
---

Interface for classes whose instances can be written to and restored from a `Parcel`. Classes implementing the Parcelable interface must also have a non-null public static field called `CREATOR` of a type that implements the `Parcelable.Creator` interface.

A typical implementation of Parcelable is:

[Kotlin](https://developer.android.com/reference/android/os/Parcelable#kotlin)[Java](https://developer.android.com/reference/android/os/Parcelable#java)

```
 class MyParcelable private constructor(`in`: Parcel) : Parcelable {
     private val mData: Int = `in`.readInt()

     override fun describeContents(): Int {
         return 0
     }

     override fun writeToParcel(out: Parcel, flags: Int) {
         out.writeInt(mData)
     }

     companion object CREATOR: Parcelable.Creator<MyParcelable?> {
         override fun createFromParcel(`in`: Parcel): MyParcelable? {
             return MyParcelable(`in`)
         }

         override fun newArray(size: Int): Array<MyParcelable?> {
             return arrayOfNulls(size)
         }
     }
 }
 
```

<br/>

## Summary

<br/>

|### Nested classes|                                                                                                                                                                         |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`interface`       |`Parcelable.ClassLoaderCreator<T>`<br><br>Specialization of `Creator` that allows you to receive the ClassLoader the object is being created in.                         |
|`interface`       |`Parcelable.Creator<T>`<br><br>Interface that must be implemented and provided as a public CREATOR field that generates instances of your Parcelable class from a Parcel.|

<br/>

|### Constants|                                                                                                                                                                                                                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`int`        |`CONTENTS_FILE_DESCRIPTOR`<br><br>Descriptor bit used with `describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.                                                                                                                 |
|`int`        |`PARCELABLE_WRITE_RETURN_VALUE`<br><br>Flag for use with `writeToParcel(Parcel, int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`".|

<br/>

|### Public methods|                                                                                                                                   |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|`abstract int`    |`describeContents()`<br><br>Describe the kinds of special objects contained in this Parcelable instance's marshaled representation.|
|`abstract void`   |`writeToParcel(Parcel dest, int flags)`<br><br>Flatten this object in to a Parcel.                                                 |

<br/>

## Constants

### CONTENTS\_FILE\_DESCRIPTOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int CONTENTS_FILE_DESCRIPTOR
```

Descriptor bit used with `describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br/>

**See also:**

*   `describeContents()`

Constant Value: 1 (0x00000001)

### PARCELABLE\_WRITE\_RETURN\_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int PARCELABLE_WRITE_RETURN_VALUE
```

Flag for use with `writeToParcel(Parcel, int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br/>

Constant Value: 1 (0x00000001)

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public abstract int describeContents ()
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `writeToParcel(android.os.Parcel, int)`, the return value of this method must include the `CONTENTS_FILE_DESCRIPTOR` bit.

<br/>

<br/>

|Returns|                                                                                                                                                                 |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`int`  |a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or `CONTENTS_FILE_DESCRIPTOR`<br><br><br/>|

<br/>

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public abstract void writeToParcel (Parcel dest, 
                int flags)
```

Flatten this object in to a Parcel.

<br/>

<br/>

|Parameters|                                                                                                                                                                                                                                             |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`dest`    |`Parcel`: The Parcel in which the object should be written. This value cannot be `null`.<br><br><br/>                                                                                                                                        |
|`flags`   |`int`: Additional flags about how the object should be written. May be 0 or `PARCELABLE_WRITE_RETURN_VALUE`. Value is either `0` or a combination of `PARCELABLE_WRITE_RETURN_VALUE`, and android.os.Parcelable.PARCELABLE\_ELIDE\_DUPLICATES|

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBQW5kcm9pZEFzeW5jJTNBJTNBdXNlcnRlc3Rpbmctc3dpbW0=/docs/upfqa3gp).
