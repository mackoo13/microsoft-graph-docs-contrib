---
title: "directRoutingLogRow resource type"
description: "Represents a row of data in the direct routing call log."
author: "mcm223"
ms.localizationpriority: medium
ms.prod: "cloud-communications"
doc_type: "resourcePageType"
---

# directRoutingLogRow resource type

Namespace: microsoft.graph.callRecords

Represents a row of data in the direct routing call log. Each row maps to one call.

## Methods

| Method       | Return Type | Description |
|:-------------|:------------|:------------|
| [getDirectRoutingCalls](../api/callrecords-callrecord-getdirectroutingcalls.md) | [microsoft.graph.callRecords.directRoutingLogRow collection](callrecords-directroutinglogrow.md)| List **directRoutingLogRow** objects for a call record. |

## Properties

|Property|Type|Description|
|:---|:---|:---|
|callEndSubReason|Int32| In addition to the SIP codes, Microsoft has own subcodes that indicate the specific issue.|
|callType|String| Call type and direction.|
|calleeNumber|String| Number of the user or bot who received the call. [E.164](https://en.wikipedia.org/wiki/E.164) format, but may include other data.|
|callerNumber|String| Number of the user or bot who made the call. [E.164](https://en.wikipedia.org/wiki/E.164) format, but may include other data.|
|correlationId|String|Identifier for the call that you can use when calling Microsoft Support. GUID.|
|duration|Int32| Duration of the call in seconds.|
|endDateTime|DateTimeOffset| Only exists for successful (fully established) calls. Time when call ended.|
|failureDateTime|DateTimeOffset| Only exists for failed (not fully established) calls.|
|finalSipCodePhrase|String| Description of the SIP code and Microsoft subcode.|
|finalSipCode|Int32| The code with which the call ended, see [RFC 3261](https://tools.ietf.org/html/rfc3261).|
|id|String|Unique call identifier. GUID.|
|inviteDateTime|DateTimeOffset| When the initial invite was sent.|
|mediaBypassEnabled|Boolean| Indicates if the trunk was enabled for media bypass or not.|
|mediaPathLocation|String| The datacenter used for media path in nonbypass call.|
|signalingLocation|String| The datacenter used for signaling for both bypass and nonbypass calls.|
|startDateTime|DateTimeOffset|Call start time.<br/>For failed and unanswered calls, this can be equal to invite or failure time.|
|successfulCall|Boolean| Success or attempt.|
|trunkFullyQualifiedDomainName|String| Fully qualified domain name of the session border controller.|
|userDisplayName|String|Display name of the user.|
|userId|String|Calling user's ID in Graph. This and other user info will be null/empty for bot call types. GUID.|
|userPrincipalName|String|UserPrincipalName (sign-in name) in Azure Active Directory. This is usually the same as user's SIP Address, and can be same as user's e-mail address.|

## Relationships

None.

## JSON representation

Here's a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.callRecords.directRoutingLogRow",
  "keyProperty": "id"
}
-->

``` json
{
  "@odata.type": "#microsoft.graph.callRecords.directRoutingLogRow",
  "calleeNumber": "String",
  "callEndSubReason": "Integer",
  "callerNumber": "String",
  "callType": "String",
  "correlationId": "String",
  "duration": "Integer",
  "endDateTime": "String (timestamp)",
  "failureDateTime": "String (timestamp)",
  "finalSipCode": "Integer",
  "finalSipCodePhrase": "String",
  "id": "String (identifier)",
  "inviteDateTime": "String (timestamp)",
  "mediaBypassEnabled": "Boolean",
  "mediaPathLocation": "String",
  "signalingLocation": "String",
  "startDateTime": "String (timestamp)",
  "successfulCall": "Boolean",
  "trunkFullyQualifiedDomainName": "String",
  "userDisplayName": "String",
  "userId": "String",
  "userPrincipalName": "String"
}
```


