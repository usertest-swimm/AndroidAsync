---
id: 2ny5le35
title: Binder
file_version: 1.1.3
app_version: 1.12.1
---

Base class for a remotable object, the core part of a lightweight remote procedure call mechanism defined by `IBinder`. This class is an implementation of IBinder that provides standard local implementation of such an object.

Most developers will not implement this class directly, instead using the [aidl](https://developer.android.com/guide/components/aidl) tool to describe the desired interface, having it generate the appropriate Binder subclass. You can, however, derive directly from Binder to implement your own custom RPC protocol or simply instantiate a raw Binder object directly to use as a token that can be shared across processes.

This class is just a basic IPC primitive; it has no impact on an application's lifecycle, and is valid only as long as the process that created it continues to run. To use this correctly, you must be doing so within the context of a top-level application component (a `Service`, `Activity`, or `ContentProvider`) that lets the system know your process should remain running.

You must keep in mind the situations in which your process could go away, and thus require that you later re-create a new Binder and re-attach it when the process starts again. For example, if you are using this within an `Activity`, your activity's process may be killed any time the activity is not started; if the activity is later re-created you will need to create a new Binder and hand it back to the correct place again; you need to be aware that your process may be started for another reason (for example to receive a broadcast) that will not involve re-creating the activity and thus run its code to create a new Binder.

**See also:**

*   `IBinder`

## Summary

<br/>

|### Inherited constants            |
|-----------------------------------|
|From interface `android.os.IBinder`|

<br/>

|### Public constructors                                           |                                                                                                                |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
|`Binder()`<br><br>Default constructor just initializes the object.|<br/>                                                                                                           |
|<br/>                                                             |`Binder(String descriptor)`<br><br>Constructor for creating a raw Binder object (token) along with a descriptor.|

<br/>

|### Public methods       |                                                                                                                                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`void`                   |`attachInterface(IInterface owner, String descriptor)`<br><br>Convenience method for associating a specific interface with the Binder.                                                                                |
|`static final long`      |`clearCallingIdentity()`<br><br>Reset the identity of the incoming IPC on the current thread.                                                                                                                         |
|`static final long`      |`clearCallingWorkSource()`<br><br>Clears the work source on this thread.                                                                                                                                              |
|`void`                   |`dump(FileDescriptor fd, String[] args)`<br><br>Implemented to call the more convenient version `dump(java.io.FileDescriptor, java.io.PrintWriter, java.lang.String[])`.                                              |
|`void`                   |`dumpAsync(FileDescriptor fd, String[] args)`<br><br>Like `dump(java.io.FileDescriptor, java.lang.String[])`, but ensures the target executes asynchronously.                                                         |
|`static final void`      |`flushPendingCommands()`<br><br>Flush any Binder commands pending in the current thread to the kernel driver.                                                                                                         |
|`static final int`       |`getCallingPid()`<br><br>Return the ID of the process that sent you the current transaction that is being processed.                                                                                                  |
|`static final int`       |`getCallingUid()`<br><br>Return the Linux UID assigned to the process that sent you the current transaction that is being processed.                                                                                  |
|`static final int`       |`getCallingUidOrThrow()`<br><br>Return the Linux UID assigned to the process that sent the transaction currently being processed.                                                                                     |
|`static final UserHandle`|`getCallingUserHandle()`<br><br>Return the UserHandle assigned to the process that sent you the current transaction that is being processed.                                                                          |
|`static final int`       |`getCallingWorkSourceUid()`<br><br>Returns the work source set by the caller.                                                                                                                                         |
|`String`                 |`getInterfaceDescriptor()`<br><br>Default implementation returns an empty interface name.                                                                                                                             |
|`boolean`                |`isBinderAlive()`<br><br>Check to see if the process that the binder is in is still alive. Note that if you're calling on a local binder, this always returns true because your process is alive if you're calling it.|
|`static final void`      |`joinThreadPool()`<br><br>Add the calling thread to the IPC thread pool.                                                                                                                                              |
|`void`                   |`linkToDeath(IBinder.DeathRecipient recipient, int flags)`<br><br>Local implementation is a no-op.                                                                                                                    |
|`boolean`                |`pingBinder()`<br><br>Default implementation always returns true -- if you got here, the object is alive.                                                                                                             |
|`IInterface`             |`queryLocalInterface(String descriptor)`<br><br>Use information supplied to `attachInterface()` to return the associated `IInterface` if it matches the requested descriptor.                                         |
|`static final void`      |`restoreCallingIdentity(long token)`<br><br>Restore the identity of the incoming IPC on the current thread back to a previously identity that was returned by `clearCallingIdentity()`.                               |
|`static final void`      |`restoreCallingWorkSource(long token)`<br><br>Restores the work source on this thread using a token returned by `setCallingWorkSourceUid(int)` or `clearCallingWorkSource()`.                                         |
|`static final long`      |`setCallingWorkSourceUid(int workSource)`<br><br>Sets the work source for this thread.                                                                                                                                |
|`final boolean`          |`transact(int code, Parcel data, Parcel reply, int flags)`<br><br>Default implementation rewinds the parcels and calls onTransact.                                                                                    |
|`boolean`                |`unlinkToDeath(IBinder.DeathRecipient recipient, int flags)`<br><br>Local implementation is a no-op.                                                                                                                  |

<br/>

|### Protected methods|                                                                                                                        |
|---------------------|------------------------------------------------------------------------------------------------------------------------|
|`void`               |`dump(FileDescriptor fd, PrintWriter fout, String[] args)`<br><br>Print the object's state into the given stream.       |
|`boolean`            |`onTransact(int code, Parcel data, Parcel reply, int flags)`<br><br>Default implementation is a stub that returns false.|

<br/>

|<br/>                              |### Inherited methods|
|-----------------------------------|---------------------|
|From class `java.lang.Object`      |                     |
|From interface `android.os.IBinder`|                     |

<br/>

## Public constructors

### Binder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public Binder ()
```

Default constructor just initializes the object.

If you're creating a Binder token (a Binder object without an attached interface), you should use `Binder(java.lang.String)` instead.

<br/>

### Binder

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public Binder (String descriptor)
```

Constructor for creating a raw Binder object (token) along with a descriptor.

The descriptor of binder objects usually specifies the interface they are implementing. In case of binder tokens, no interface is implemented, and the descriptor can be used as a sort of tag to help identify the binder token. This will help identify remote references to these objects more easily when debugging.

<br/>

<br/>

|Parameters  |                                                                                                                                                                                                                                      |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`descriptor`|`String`: Used to identify the creator of this token, for example the class name. Instead of creating multiple tokens with the same descriptor, consider adding a suffix to help identify them. This value may be `null`.<br><br><br/>|

<br/>

## Public methods

### attachInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public void attachInterface (IInterface owner, 
                String descriptor)
```

Convenience method for associating a specific interface with the Binder. After calling, `queryLocalInterface()` will be implemented for you to return the given owner IInterface when the corresponding descriptor is requested.

<br/>

<br/>

|Parameters  |                                                    |
|------------|----------------------------------------------------|
|`owner`     |`IInterface`: This value may be `null`.<br><br><br/>|
|`descriptor`|`String`: This value may be `null`.<br><br><br/>    |

<br/>

### clearCallingIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final long clearCallingIdentity ()
```

Reset the identity of the incoming IPC on the current thread. This can be useful if, while handling an incoming call, you will be calling on interfaces of other objects that may be local to your process and need to do permission checks on the calls coming into them (so they will check the permission of your own local process, and not whatever process originally called you).

<br/>

<br/>

|Returns|                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
|`long` |Returns an opaque token that can be used to restore the original calling identity by passing it to `restoreCallingIdentity(long)`.<br><br><br/>|

<br/>

**See also:**

*   `getCallingPid()`

*   `getCallingUid()`

*   `restoreCallingIdentity(long)`

### clearCallingWorkSource

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final long clearCallingWorkSource ()
```

Clears the work source on this thread.

The work source will be propagated for future outgoing binder transactions executed on this thread.

`restoreCallingWorkSource(long)` must always be called after clearing the worksource.

A typical use case would be

```
 long token = Binder.clearCallingWorkSource();
 try {
   // Call an API.
 } finally {
   Binder.restoreCallingWorkSource(token);
 }
 
```

<br/>

<br/>

<br/>

|Returns|                                                   |
|-------|---------------------------------------------------|
|`long` |token to restore original work source.<br><br><br/>|

<br/>

### dump

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public void dump (FileDescriptor fd, 
                String[] args)
```

Implemented to call the more convenient version `dump(java.io.FileDescriptor, java.io.PrintWriter, java.lang.String[])`.

<br/>

<br/>

|Parameters|                                                           |
|----------|-----------------------------------------------------------|
|`fd`      |`FileDescriptor`: This value cannot be `null`.<br><br><br/>|
|`args`    |`String`: This value may be `null`.<br><br><br/>           |

<br/>

### dumpAsync

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public void dumpAsync (FileDescriptor fd, 
                String[] args)
```

Like `dump(java.io.FileDescriptor, java.lang.String[])`, but ensures the target executes asynchronously.

<br/>

<br/>

|Parameters|                                                           |
|----------|-----------------------------------------------------------|
|`fd`      |`FileDescriptor`: This value cannot be `null`.<br><br><br/>|
|`args`    |`String`: This value may be `null`.<br><br><br/>           |

<br/>

### flushPendingCommands

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final void flushPendingCommands ()
```

Flush any Binder commands pending in the current thread to the kernel driver. This can be useful to call before performing an operation that may block for a long time, to ensure that any pending object references have been released in order to prevent the process from holding on to objects longer than it needs to.

<br/>

### getCallingPid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int getCallingPid ()
```

Return the ID of the process that sent you the current transaction that is being processed. This PID can be used with higher-level system services to determine its identity and check permissions. If the current thread is not currently executing an incoming transaction, then its own PID is returned. Warning: oneway transactions do not receive PID.

<br/>

<br/>

|Returns|     |
|-------|-----|
|`int`  |<br/>|

<br/>

### getCallingUid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int getCallingUid ()
```

Return the Linux UID assigned to the process that sent you the current transaction that is being processed. This UID can be used with higher-level system services to determine its identity and check permissions. If the current thread is not currently executing an incoming transaction, then its own UID is returned.

<br/>

<br/>

|Returns|     |
|-------|-----|
|`int`  |<br/>|

<br/>

### getCallingUidOrThrow

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int getCallingUidOrThrow ()
```

Return the Linux UID assigned to the process that sent the transaction currently being processed.

<br/>

<br/>

|Returns|     |
|-------|-----|
|`int`  |<br/>|

<br/>

|Throws                 |                                                                                                                                                           |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
|`IllegalStateException`|if the current thread is not currently executing an incoming transaction and the calling identity has not been explicitly set with `clearCallingIdentity()`|

<br/>

### getCallingUserHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final UserHandle getCallingUserHandle ()
```

Return the UserHandle assigned to the process that sent you the current transaction that is being processed. This is the user of the caller. It is distinct from `getCallingUid()` in that a particular user will have multiple distinct apps running under it each with their own UID. If the current thread is not currently executing an incoming transaction, then its own UserHandle is returned.

<br/>

<br/>

|Returns     |                                         |
|------------|-----------------------------------------|
|`UserHandle`|This value cannot be `null`.<br><br><br/>|

<br/>

**See also:**

*   `UserHandle`

### getCallingWorkSourceUid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final int getCallingWorkSourceUid ()
```

Returns the work source set by the caller.

Unlike `getCallingUid()`, this result of this method cannot be trusted. The caller can set the value to whatever they want. Only use this value if you trust the calling UID.

<br/>

<br/>

|Returns|                                                                     |
|-------|---------------------------------------------------------------------|
|`int`  |The original UID responsible for the binder transaction.<br><br><br/>|

<br/>

### getInterfaceDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public String getInterfaceDescriptor ()
```

Default implementation returns an empty interface name.

<br/>

<br/>

|Returns |                                      |
|--------|--------------------------------------|
|`String`|This value may be `null`.<br><br><br/>|

<br/>

### isBinderAlive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public boolean isBinderAlive ()
```

Check to see if the process that the binder is in is still alive. Note that if you're calling on a local binder, this always returns true because your process is alive if you're calling it.

<br/>

<br/>

|Returns  |                                                                                                                                    |
|---------|------------------------------------------------------------------------------------------------------------------------------------|
|`boolean`|false if the process is not alive. Note that if it returns true, the process may have died while the call is returning.<br><br><br/>|

<br/>

### joinThreadPool

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final void joinThreadPool ()
```

Add the calling thread to the IPC thread pool. This function does not return until the current process is exiting.

<br/>

### linkToDeath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public void linkToDeath (IBinder.DeathRecipient recipient, 
                int flags)
```

Local implementation is a no-op.

<br/>

<br/>

|Parameters |                                                                   |
|-----------|-------------------------------------------------------------------|
|`recipient`|`IBinder.DeathRecipient`: This value cannot be `null`.<br><br><br/>|
|`flags`    |`int`<br><br><br/>                                                 |

<br/>

### pingBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public boolean pingBinder ()
```

Default implementation always returns true -- if you got here, the object is alive.

<br/>

<br/>

|Returns  |                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`boolean`|Returns false if the hosting process is gone, otherwise the result (always by default true) returned by the pingBinder() implementation on the other side.<br><br><br/>|

<br/>

### queryLocalInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public IInterface queryLocalInterface (String descriptor)
```

Use information supplied to `attachInterface()` to return the associated `IInterface` if it matches the requested descriptor.

<br/>

<br/>

|Parameters  |                                                   |
|------------|---------------------------------------------------|
|`descriptor`|`String`: This value cannot be `null`.<br><br><br/>|

<br/>

|Returns     |                                      |
|------------|--------------------------------------|
|`IInterface`|This value may be `null`.<br><br><br/>|

<br/>

### restoreCallingIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final void restoreCallingIdentity (long token)
```

Restore the identity of the incoming IPC on the current thread back to a previously identity that was returned by `clearCallingIdentity()`.

<br/>

<br/>

|Parameters|                                                                                               |
|----------|-----------------------------------------------------------------------------------------------|
|`token`   |`long`: The opaque token that was previously returned by `clearCallingIdentity()`.<br><br><br/>|

<br/>

**See also:**

*   `clearCallingIdentity()`

### restoreCallingWorkSource

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final void restoreCallingWorkSource (long token)
```

Restores the work source on this thread using a token returned by `setCallingWorkSourceUid(int)` or `clearCallingWorkSource()`.

A typical use case would be

```
 long token = Binder.setCallingWorkSourceUid(uid);
 try {
   // Call an API.
 } finally {
   Binder.restoreCallingWorkSource(token);
 }
 
```

<br/>

<br/>

<br/>

|Parameters|                   |
|----------|-------------------|
|`token`   |`long`<br><br><br/>|

<br/>

### setCallingWorkSourceUid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public static final long setCallingWorkSourceUid (int workSource)
```

Sets the work source for this thread.

All the following binder calls on this thread will use the provided work source. If this is called during an on-going binder transaction, all the following binder calls will use the work source until the end of the transaction.

The concept of worksource is similar to `WorkSource`. However, for performance reasons, we only support one UID. This UID represents the original user responsible for the binder calls.

`restoreCallingWorkSource(long)` must always be called after setting the worksource.

A typical use case would be

```
 long token = Binder.setCallingWorkSourceUid(uid);
 try {
   // Call an API.
 } finally {
   Binder.restoreCallingWorkSource(token);
 }
 
```

The work source will be propagated for future outgoing binder transactions executed on this thread.

<br/>

<br/>

|Parameters  |                                                                     |
|------------|---------------------------------------------------------------------|
|`workSource`|`int`: The original UID responsible for the binder call.<br><br><br/>|

<br/>

|Returns|                                                   |
|-------|---------------------------------------------------|
|`long` |token to restore original work source.<br><br><br/>|

<br/>

### transact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public final boolean transact (int code, 
                Parcel data, 
                Parcel reply, 
                int flags)
```

Default implementation rewinds the parcels and calls onTransact. On the remote side, transact calls into the binder to do the IPC.

<br/>

<br/>

|Parameters|                                                                                                                                                |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
|`code`    |`int`: The action to perform. This should be a number between `IBinder.FIRST_CALL_TRANSACTION` and `IBinder.LAST_CALL_TRANSACTION`.<br><br><br/>|
|`data`    |`Parcel`: This value cannot be `null`.<br><br><br/>                                                                                             |
|`reply`   |`Parcel`: This value may be `null`.<br><br><br/>                                                                                                |
|`flags`   |`int`: Additional operation flags. Either 0 for a normal RPC, or `IBinder.FLAG_ONEWAY` for a one-way RPC.<br><br><br/>                          |

<br/>

|Returns  |                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`boolean`|Returns the result from `Binder#onTransact`. A successful call generally returns true; false generally means the transaction code was not understood. For a oneway call to a different process false should never be returned. If a oneway call is made to code in the same process (usually to a C++ or Rust implementation), then there are no oneway semantics, and false can still be returned.<br><br><br/>|

<br/>

|Throws           |     |
|-----------------|-----|
|`RemoteException`|<br/>|

<br/>

### unlinkToDeath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
public boolean unlinkToDeath (IBinder.DeathRecipient recipient, 
                int flags)
```

Local implementation is a no-op.

<br/>

<br/>

|Parameters |                                                                   |
|-----------|-------------------------------------------------------------------|
|`recipient`|`IBinder.DeathRecipient`: This value cannot be `null`.<br><br><br/>|
|`flags`    |`int`<br><br><br/>                                                 |

<br/>

|Returns  |                                                                                                                                                                                                                                                       |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`boolean`|`true` if the **recipient** is successfully unlinked, assuring you that its `DeathRecipient.binderDied()` method will not be called; `false` if the target IBinder has already died, meaning the method has been (or soon will be) called.<br><br><br/>|

<br/>

## Protected methods

### dump

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
protected void dump (FileDescriptor fd, 
                PrintWriter fout, 
                String[] args)
```

Print the object's state into the given stream.

<br/>

<br/>

|Parameters|                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
|`fd`      |`FileDescriptor`: The raw file descriptor that the dump is being sent to. This value cannot be `null`.<br><br><br/>                                 |
|`fout`    |`PrintWriter`: The file to which you should dump your state. This will be closed for you after you return. This value cannot be `null`.<br><br><br/>|
|`args`    |`String`: additional arguments to the dump request. This value may be `null`.<br><br><br/>                                                          |

<br/>

### onTransact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)

```
protected boolean onTransact (int code, 
                Parcel data, 
                Parcel reply, 
                int flags)
```

Default implementation is a stub that returns false. You will want to override this to do the appropriate unmarshalling of transactions.

If you want to call this, call transact().

Implementations that are returning a result should generally use `Parcel.writeNoException` and `Parcel.writeException` to propagate exceptions back to the caller.

<br/>

<br/>

|Parameters|                                                                                                                                                |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
|`code`    |`int`: The action to perform. This should be a number between `IBinder.FIRST_CALL_TRANSACTION` and `IBinder.LAST_CALL_TRANSACTION`.<br><br><br/>|
|`data`    |`Parcel`: Marshalled data being received from the caller. This value cannot be `null`.<br><br><br/>                                             |
|`reply`   |`Parcel`: If the caller is expecting a result back, it should be marshalled in to here. This value may be `null`.<br><br><br/>                  |
|`flags`   |`int`: Additional operation flags. Either 0 for a normal RPC, or `IBinder.FLAG_ONEWAY` for a one-way RPC.<br><br><br/>                          |

<br/>

|Returns  |                                                                                                                                 |
|---------|---------------------------------------------------------------------------------------------------------------------------------|
|`boolean`|Return true on a successful call; returning false is generally used to indicate that you did not understand the transaction code.|

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBQW5kcm9pZEFzeW5jJTNBJTNBdXNlcnRlc3Rpbmctc3dpbW0=/docs/2ny5le35).
