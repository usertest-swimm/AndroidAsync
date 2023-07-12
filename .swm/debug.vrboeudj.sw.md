---
id: vrboeudj
title: Debug
file_version: 1.1.3
app_version: 1.12.1
---

Provides various debugging methods for Android applications, including tracing and allocation counts.

**Logging Trace Files**

Debug can create log files that give details about an application, such as a call stack and start/stop times for any running methods. See [Inspect Trace Logs with Traceview](https://developer.android.com/studio/profile/traceview) for information about reading trace files. To start logging trace files, call one of the startMethodTracing() methods. To stop tracing, call `stopMethodTracing()`.

## Summary

<br/>

|### Nested classes|                                                                                                                         |
|------------------|-------------------------------------------------------------------------------------------------------------------------|
|`class`           |`Debug.InstructionCount`<br><br>_This class was deprecated in API level 23. Instruction counting is no longer supported._|
|`class`           |`Debug.MemoryInfo`<br><br>This class is used to retrieved various statistics about the memory mappings for this process. |

<br/>

|### Constants|                                                                                                                                            |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
|`int`        |`SHOW_CLASSLOADER`<br><br><br/>                                                                                                             |
|`int`        |`SHOW_FULL_DETAIL`<br><br>Flags for printLoadedClasses().                                                                                   |
|`int`        |`SHOW_INITIALIZED`<br><br><br/>                                                                                                             |
|`int`        |`TRACE_COUNT_ALLOCS`<br><br>_This constant was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._|

<br/>

|### Public methods          |                                                                                                                                                                                                            |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`static void`               |`attachJvmtiAgent(String library, String options, ClassLoader classLoader)`<br><br>Attach a library as a jvmti agent to the current runtime, with the given classloader determining the library search path.|
|`static void`               |`changeDebugPort(int port)`<br><br>_This method was deprecated in API level 15. no longer needed or useful_                                                                                                 |
|`static void`               |`dumpHprofData(String fileName)`<br><br>Dump "hprof" data to the specified file.                                                                                                                            |
|`static boolean`            |`dumpService(String name, FileDescriptor fd, String[] args)`<br><br>Get a debugging dump of a system service by name.                                                                                       |
|`static void`               |`enableEmulatorTraceOutput()`<br><br>_This method was deprecated in API level 34. Please use other tracing method in this class._                                                                           |
|`static int`                |`getBinderDeathObjectCount()`<br><br>Returns the number of death notification links to Binder objects that exist in the current process.                                                                    |
|`static int`                |`getBinderLocalObjectCount()`<br><br>Returns the number of active local Binder objects that exist in the current process.                                                                                   |
|`static int`                |`getBinderProxyObjectCount()`<br><br>Returns the number of references to remote proxy Binder objects that exist in the current process.                                                                     |
|`static int`                |`getBinderReceivedTransactions()`<br><br>Returns the number of received transactions from the binder driver.                                                                                                |
|`static int`                |`getBinderSentTransactions()`<br><br>Returns the number of sent transactions from this process.                                                                                                             |
|`static int`                |`getGlobalAllocCount()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                               |
|`static int`                |`getGlobalAllocSize()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                                |
|`static int`                |`getGlobalClassInitCount()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                           |
|`static int`                |`getGlobalClassInitTime()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                            |
|`static int`                |`getGlobalExternalAllocCount()`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                           |
|`static int`                |`getGlobalExternalAllocSize()`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                            |
|`static int`                |`getGlobalExternalFreedCount()`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                           |
|`static int`                |`getGlobalExternalFreedSize()`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                            |
|`static int`                |`getGlobalFreedCount()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                               |
|`static int`                |`getGlobalFreedSize()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                                |
|`static int`                |`getGlobalGcInvocationCount()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                        |
|`static int`                |`getLoadedClassCount()`<br><br>Get the number of loaded classes.                                                                                                                                            |
|`static void`               |`getMemoryInfo(Debug.MemoryInfo memoryInfo)`<br><br>Retrieves information about this processes memory usages.                                                                                               |
|`static long`               |`getNativeHeapAllocatedSize()`<br><br>Returns the amount of allocated memory in the native heap.                                                                                                            |
|`static long`               |`getNativeHeapFreeSize()`<br><br>Returns the amount of free memory in the native heap.                                                                                                                      |
|`static long`               |`getNativeHeapSize()`<br><br>Returns the size of the native heap.                                                                                                                                           |
|`static long`               |`getPss()`<br><br>Retrieves the PSS memory used by the process as given by the smaps.                                                                                                                       |
|`static String`             |`getRuntimeStat(String statName)`<br><br>Returns the value of a particular runtime statistic or `null` if no such runtime statistic exists.                                                                 |
|`static Map<String, String>`|`getRuntimeStats()`<br><br>Returns a map of the names/values of the runtime statistics that `getRuntimeStat(java.lang.String)` supports.                                                                    |
|`static int`                |`getThreadAllocCount()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                               |
|`static int`                |`getThreadAllocSize()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                                |
|`static int`                |`getThreadExternalAllocCount()`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                           |
|`static int`                |`getThreadExternalAllocSize()`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                            |
|`static int`                |`getThreadGcInvocationCount()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                        |
|`static boolean`            |`isDebuggerConnected()`<br><br>Determine if a debugger is currently attached.                                                                                                                               |
|`static void`               |`printLoadedClasses(int flags)`<br><br>Dump a list of all currently loaded class to the log file.                                                                                                           |
|`static void`               |`resetAllCounts()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                                    |
|`static void`               |`resetGlobalAllocCount()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                             |
|`static void`               |`resetGlobalAllocSize()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                              |
|`static void`               |`resetGlobalClassInitCount()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                         |
|`static void`               |`resetGlobalClassInitTime()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                          |
|`static void`               |`resetGlobalExternalAllocCount()`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                         |
|`static void`               |`resetGlobalExternalAllocSize()`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                          |
|`static void`               |`resetGlobalExternalFreedCount()`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                         |
|`static void`               |`resetGlobalExternalFreedSize()`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                          |
|`static void`               |`resetGlobalFreedCount()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                             |
|`static void`               |`resetGlobalFreedSize()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                              |
|`static void`               |`resetGlobalGcInvocationCount()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                      |
|`static void`               |`resetThreadAllocCount()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                             |
|`static void`               |`resetThreadAllocSize()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                              |
|`static void`               |`resetThreadExternalAllocCount()`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                         |
|`static void`               |`resetThreadExternalAllocSize()`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                          |
|`static void`               |`resetThreadGcInvocationCount()`<br><br>_This method was deprecated in API level 23. Accurate counting is a burden on the runtime and may be removed._                                                      |
|`static int`                |`setAllocationLimit(int limit)`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                           |
|`static int`                |`setGlobalAllocationLimit(int limit)`<br><br>_This method was deprecated in API level 15. This method is now obsolete._                                                                                     |
|`static void`               |`startAllocCounting()`<br><br>_This method was deprecated in API level 18. Accurate counting is a burden on the runtime and may be removed._                                                                |
|`static void`               |`startMethodTracing()`<br><br>Start method tracing with default log name and buffer size.                                                                                                                   |
|`static void`               |`startMethodTracing(String tracePath, int bufferSize, int flags)`<br><br>Start method tracing, specifying the trace log file name, the buffer size, and flags.                                              |
|`static void`               |`startMethodTracing(String tracePath)`<br><br>Start method tracing, specifying the trace log file path.                                                                                                     |
|`static void`               |`startMethodTracing(String tracePath, int bufferSize)`<br><br>Start method tracing, specifying the trace log file name and the buffer size.                                                                 |
|`static void`               |`startMethodTracingSampling(String tracePath, int bufferSize, int intervalUs)`<br><br>Start sampling-based method tracing, specifying the trace log file name, the buffer size, and the sampling interval.  |
|`static void`               |`startNativeTracing()`<br><br>Enable qemu tracing.                                                                                                                                                          |
|`static void`               |`stopAllocCounting()`<br><br>_This method was deprecated in API level 18. Accurate counting is a burden on the runtime and may be removed._                                                                 |
|`static void`               |`stopMethodTracing()`<br><br>Stop method tracing.                                                                                                                                                           |
|`static void`               |`stopNativeTracing()`<br><br>Stop qemu tracing.                                                                                                                                                             |
|`static long`               |`threadCpuTimeNanos()`<br><br>Get an indication of thread CPU usage.                                                                                                                                        |
|`static void`               |`waitForDebugger()`<br><br>Wait until a debugger attaches.                                                                                                                                                  |
|`static boolean`            |`waitingForDebugger()`<br><br>Returns "true" if one or more threads is waiting for a debugger to attach.                                                                                                    |

<br/>

|<br/>                        |### Inherited methods|
|-----------------------------|---------------------|
|From class `java.lang.Object`|                     |

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBQW5kcm9pZEFzeW5jJTNBJTNBdXNlcnRlc3Rpbmctc3dpbW0=/docs/vrboeudj).
