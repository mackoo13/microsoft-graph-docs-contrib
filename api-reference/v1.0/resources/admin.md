---
title: "admin resource type"
description: "Represents an entity that acts as a container for administrator functionality."
author: "angelgolfer-ms"
ms.localizationpriority: medium
ms.prod: "service-communications"
doc_type: resourcePageType
---

# admin resource type

Namespace: microsoft.graph

Represents an entity that acts as a container for administrator functionality.

## Properties
None.

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
| edge | [edge](edge.md) | A container for Microsoft Edge resources. Read-only. |
| serviceAnnouncement | [serviceAnnouncement](serviceannouncement.md) | A container for service communications resources. Read-only. |
| sharepointSettings | [sharepointSettings](../resources/sharepointSettings.md) | A container for administrative resources to manage tenant-level settings for SharePoint and OneDrive. |


## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.admin",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.admin"
}
```
