---
title: "voiceAuthenticationMethodTarget resource type"
description: "A collection of groups enabled to use voice call authentication method via policy."
author: "luc-msft"
ms.localizationpriority: medium
ms.prod: "identity-and-sign-in"
doc_type: resourcePageType
---

# voiceAuthenticationMethodTarget resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A collection of groups enabled to use voice call authentication via the [voice call authentication methods policy](../resources/voiceAuthenticationMethodConfiguration.md) in Azure AD.

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|Object ID of an Azure AD group.|
|isRegistrationRequired|Boolean|Determines whether the user is enforced to register the authentication method. **Not supported**.|
|targetType|authenticationMethodTargetType|Possible values are: `group`, and `unknownFutureValue`. From December 2022, targeting individual users using `user` is no longer recommended. Existing targets remain but we recommend moving the individual users to a targeted group. Inherited from [authenticationMethodTarget](authenticationMethodTarget.md).|

## Relationships
None.

## JSON representation
Here's a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.voiceAuthenticationMethodTarget",
  "baseType": "microsoft.graph.authenticationMethodTarget",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.voiceAuthenticationMethodTarget",
  "id": "String (identifier)",
  "targetType": "String",
  "isRegistrationRequired": "Boolean"
}
```

