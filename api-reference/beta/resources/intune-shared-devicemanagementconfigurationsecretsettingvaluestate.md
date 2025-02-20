---
title: "deviceManagementConfigurationSecretSettingValueState enum type"
description: "type tracking the encryption state of a secret setting value"
author: "jaiprakashmb"
ms.localizationpriority: medium
ms.subservice: "intune"
doc_type: enumPageType
ms.date: 08/01/2024
---

# deviceManagementConfigurationSecretSettingValueState enum type

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

type tracking the encryption state of a secret setting value

## Members
|Member|Value|Description|
|:---|:---|:---|
|invalid|0|default invalid value|
|notEncrypted|1|secret value is not encrypted|
|encryptedValueToken|2|a token for the encrypted value is returned by the service|
