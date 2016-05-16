---
title: logman update alert
ms.custom: na
ms.prod: windows-server-2012
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ede94a76-931c-40ed-9fda-6766bed8ff72
---
# logman update alert
Update the properties of an existing alert data collector.

For examples of how this command can be used, see [Examples](#BKMK_examples).

## Syntax

```
logman update alert <[-n] <name>> [options]
```

## Parameters

|Parameter|Description|
|-------------|---------------|
|\/?|Displays context\-sensitive help.|
|\-s <computer name>|Perform the command on the specified remote computer.|
|\-config <value>|Specifies the settings file containing command options.|
|\[\-n\] <name>|Name of the target object.|
|\-\[\-\]u <user \[password\]>|Specifies the user to Run As. Entering a \* for the password produces a prompt for the password. The password is not displayed when you type it at the password prompt.|
|\-m <\[start\] \[stop\] \[\[start\] \[stop\] \[...\]\]>|Change to manual start or stop instead of a scheduled begin or end time.|
|\-rf <\[\[hh:\]mm:\]ss>|Run the data collector for the specified period of time.|
|\-b <M\/d\/yyyy h:mm:ss\[AM&#124;PM\]>|Begin collecting data at the specified time.|
|\-e <M\/d\/yyyy h:mm:ss\[AM&#124;PM\]>|End data collection at the specified time.|
|\-si <\[\[hh:\]mm:\]ss>|Specifies the sample interval for performance counter data collectors.|
|\-o <path&#124;dsn\!log>|Specifies the output log file or the DSN and log set name in a SQL database.|
|\-\[\-\]r|Repeat the data collector daily at the specified begin and end times.|
|\-\[\-\]a|Append to an existing log file.|
|\-\[\-\]ow|Overwrite an existing log file.|
|\-\[\-\]v <nnnnnn&#124;mmddhhmm>|Attach file versioning information to the end of the log file name.|
|\-\[\-\]rc <task>|Run the command specified each time the log is closed.|
|\-\[\-\]max <value>|Maximum log file size in MB or maximum number of records for SQL logs.|
|\-\[\-\]cnf <\[\[hh:\]mm:\]ss>|When time is specified, create a new file when the specified time has elapsed. When time is not specified, create a new file when the maximum size is exceeded.|
|\-y|Answer yes to all questions without prompting.|
|\-cf <filename>|Specifies the file listing performance counters to collect. The file should contain one performance counter name per line.|
|\-\[\-\]el|Enables or disables Event Log reporting.|
|\-th <threshold \[threshold \[...\]\]>|Specify counters and their threshold values for an alert.|
|\-\[\-\]rdcs <name>|Specifies the Data Collector Set to start when an alert fires.|
|\-\[\-\]tn <task>|Specifies the task to run when an alert fires.|
|\-\[\-\]targ <argument>|Specifies the task arguments to be used with the task specified using \-tn.|

## Remarks
Where \[\-\] is listed, an extra \- negates the option.

## <a name="BKMK_examples"></a>Examples
The following example updates the existing data collector new\_alert, setting the threshold value for the counter % Processor Time in the Processor\(\_Total\) counter group to 40%.

```
logman update alert new_alert -th "\Processor(_Total)\% Processor Time>40"
```

#### Additional references
[Logman](Logman.md)

[logman create alert](logman-create-alert.md)

