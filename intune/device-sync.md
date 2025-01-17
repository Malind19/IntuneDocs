---
# required metadata

title: Sync devices with Microsoft Intune - Azure | Microsoft Docs
description: Synchronize devices that are registered or managed with Microsoft Intune to get the latest policies and actions. Includes the steps to sync by using the Azure portal, and lists the error codes that can be retried.
keywords:
author: ErikjeMS
ms.author: erikje
manager: dougeby
ms.date: 06/21/2019
ms.topic: conceptual
ms.service: microsoft-intune
ms.localizationpriority: high
ms.technology:
ms.assetid: 02ad249e-f098-421f-861f-6b2ff733ac7c

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
#ms.reviewer: ilwu
ms.suite: ems
search.appverid: MET150
#ms.tgt_pltfrm:
ms.custom: intune-azure
ms.collection: M365-identity-device-management
---

# Sync devices to get the latest policies and actions with Intune


[!INCLUDE [azure_portal](./includes/azure_portal.md)]

The **Sync** device action forces the selected device to immediately check in with Intune. When a device checks in, it immediately receives any pending actions or policies that have been assigned to it. This feature can help you immediately validate and troubleshoot policies you’ve assigned, without waiting for the next scheduled check-in.

## Supported platforms

- Windows
- Windows Phone
- iOS
- macOS
- Android

## Sync a device

1. Sign in to [Intune](https://go.microsoft.com/fwlink/?linkid=2090973). 
3. In **Intune**, select **Devices** > **All devices**.
4. In the list of devices you manage, select a device to open its *Overview* pane, and then select **Sync**.
5. To confirm, select **Yes**.

To see the status of the sync action, choose **Devices** > **Device actions**.

You can find standard Intune policy check-in frequencies in the [Refresh cycle times](device-profiles.md).

## Retryable error codes

When an administrator runs the **Sync** device action, iOS and Android apps that failed and raised a retryable error code are still available to the device. However, apps that raised a nonretryable error code must wait seven days before they're available to the device.


| Error code  | Suggested description | Retryable |
|---|---|---|
| 2016330898 | An unknown error occurred. | No |
| 2016330897 | Your connection to Intune timed out. Reset your connection. | Yes |
| 2016330896 | You lost connection to the Internet. Reset your connection. | Yes |
| 2016330895 | You lost connection to the Internet. Reset your connection. | Yes |
| 2016330894 | You lost connection to the Internet. Reset your connection. | Yes |
| 2016330893 | You lost connection to the Internet. Reset your connection. | Yes|
| 2016330892 | International roaming is disabled. | No|
| 2016330891 | The cellular data connection for this device cannot be accessed while a phone call is being made. Wait for the phone call to complete. | Yes|
| 2016330890 | The cellular network for this device. These devices could not be used at this time. | No|
| 2016330889 | The secure connection failed. Reset your connection. | Yes|
| 2016330888 | The server trust evaluation has failed. | No|

## Next steps

You can [check the details](device-inventory.md) of the device.
 
