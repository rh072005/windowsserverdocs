---
title: The Server cleanup Wizard
description: "Windows Server Update Service (WSUS) topic - How to use the Server cleanup Wizard to manage disk space"
ms.prod: windows-server-threshold
ms.reviewer: na
ms.suite: na
ms.technology: manage-wsus
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7c351797-2716-4442-a668-60d5b4e77751
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/12/2016
---
# The Server cleanup Wizard

>Applies To: Windows Server&reg; 2016, Windows Server&reg; 2012 R2, Windows Server&reg; 2012

The Server cleanup Wizard is integrated into the user interface and can be used to help you manage your disk space. This wizard can do the following operations:

-   remove unused updates and update revisions remove all older updates and update revisions that have not been approved.

-   delete computers not contacting the server delete all client computers that have not contacted the server in thirty days or more.

-   delete unneeded update files delete all update files that are not needed by updates or by downstream servers.

-   Decline expired updates decline all updates that have been expired by Microsoft.

-   Decline superseded updates decline all updates that meet all the following criteria:

    -   The superseded update is not mandatory

    -   The superseded update has been on the server for thirty days or more

    -   The superseded update is not currently reported as needed by any client

    -   The superseded update has not been explicitly deployed to a computer group for ninety days or more

    -   The superseding update must be approved for install to a computer group

It is important to mention that if you choose to remove unneeded content with the Server cleanup Wizard, all the private update files that you have downloaded from the Catalog Site will be removed as well. You will need to re-import these files after running the Server cleanup Wizard.

if updates are approved using an auto-approval rule, they might still be in the "Approved" state, and will not be removed by The Server cleanup Wizard. To remove auto-approved updates that are in an "approved" state , the WSUS Admin must - at minimum - manually set the approval status of superseded updates to "Not Approved" so they will be eligible for declination by the Server cleanup Wizard. The Server cleanup Wizard will ensure a newer update is approved and that no client system is still reporting that update as needed before marking the update as "Declined."



