---
title: Bitsadmin getnotifycmdline
description: "Windows Commands topic for **Bitsadmin getnotifycmdline** - Retrieves the command-line command that is ran when the job finishes transferring data."
ms.custom: na
ms.prod: windows-server-threshold
ms.reviewer: na
ms.suite: na
ms.technology: manage-windows-commands
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 90fa33e6-aca5-4a23-82bd-19a9f13f8416
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/12/2016
---
# Bitsadmin getnotifycmdline

>Applies To: Windows Server&reg; 2016, Windows Server&reg; 2012 R2, Windows Server&reg; 2012

Retrieves the command-line command that is ran when the job finishes transferring data.
## Syntax
```
bitsadmin /GetNotifyCmdLine <Job>
```
## Parameters
|Parameter|Description|
|-------|--------|
|Job|The job's display name or GUID|
## <a name="BKMK_examples"></a>Examples
The following example retrieves the command-line command used by the service when the job named *myDownloadJob* completes.
```
C:\>bitsadmin /GetNotifyCmdLine myDownloadJob
```
## Additional references
[Command-Line Syntax Key](Command-Line-Syntax-Key.md)