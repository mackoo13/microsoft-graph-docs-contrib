---
title: "accessReviewStage resource type"
description: "Represents a stage of an accessReviewInstance."
author: "isabelleatmsft"
ms.localizationpriority: medium
ms.prod: "governance"
doc_type: resourcePageType
---

# accessReviewStage resource type

Namespace: microsoft.graph

Represents a stage of an Azure AD [access review](accessreviewsv2-overview.md). If the parent [accessReviewScheduleDefinition](accessreviewscheduledefinition.md) has defined the **stageSettings** property, the [accessReviewInstance](accessReviewInstance.md) is comprised of up to three subsequent stages. Each stage may have a different set of reviewers who can act on the stage decisions, and settings determining which decisions pass from stage to stage.

Every **accessReviewStage** contains a list of [decision items](accessreviewinstancedecisionitem.md) for reviewers. There's only one decision per identity being reviewed.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List accessReviewStages](../api/accessreviewinstance-list-stages.md)|[accessReviewStage](../resources/accessreviewstage.md) collection|Get a list of the [accessReviewStage](../resources/accessreviewstage.md) objects and their properties.|
|[Get accessReviewStage](../api/accessreviewstage-get.md)|[accessReviewStage](../resources/accessreviewstage.md)|Read the properties and relationships of an [accessReviewStage](../resources/accessreviewstage.md) object.|
|[Update accessReviewStage](../api/accessreviewstage-update.md)|[accessReviewStage](../resources/accessreviewstage.md)|Update the properties of an [accessReviewStage](../resources/accessreviewstage.md) object.|
|[stop](../api/accessreviewstage-stop.md)|None|	Manually stop an accessReviewStage.|
|[filterByCurrentUser](../api/accessreviewstage-filterbycurrentuser.md)|[accessReviewStage](../resources/accessreviewstage.md) collection|Returns all stages on a given [accessReviewInstance](accessReviewInstance.md)  for which the calling user is a reviewer.|
|[List decisions](../api/accessreviewstage-list-decisions.md)|[accessReviewInstanceDecisionItem](../resources/accessreviewinstancedecisionitem.md) collection|Get the decisions made in an accessReviewStage.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|endDateTime|DateTimeOffset|The date and time in ISO 8601 format and UTC time when the review stage is scheduled to end. This property is the cumulative total of the **durationInDays** for all stages. Read-only. |
|fallbackReviewers|[accessReviewReviewerScope](../resources/accessreviewreviewerscope.md) collection|This collection of reviewer scopes is used to define the list of fallback reviewers. These fallback reviewers are notified to take action if no users are found from the list of reviewers specified. This could occur when either the group owner is specified as the reviewer but the group owner doesn't exist, or manager is specified as reviewer but a user's manager doesn't exist.|
|id|String|Unique identifier of the stage. Read-only.|
|reviewers|[accessReviewReviewerScope](../resources/accessreviewreviewerscope.md) collection|This collection of access review scopes is used to define who the reviewers are. For examples of options for assigning reviewers, see [Assign reviewers to your access review definition using the Microsoft Graph API](/graph/accessreviews-scope-concept).|
|startDateTime|DateTimeOffset|The date and time in ISO 8601 format and UTC time when the review stage is scheduled to start. Read-only. |
|status|String|Specifies the status of an accessReviewStage. Possible values: `Initializing`, `NotStarted`, `Starting`, `InProgress`, `Completing`, `Completed`, `AutoReviewing`, and `AutoReviewed`. Supports `$orderby`, and `$filter` (`eq` only). Read-only.|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|decisions|[accessReviewInstanceDecisionItem](../resources/accessreviewinstancedecisionitem.md) collection|Each user reviewed in an accessReviewStage has a decision item representing if they were approved, denied, or not yet reviewed.|

## JSON representation
Here's a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.accessReviewStage",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.accessReviewStage",
  "endDateTime": "String (timestamp)",
  "fallbackReviewers": [
    {
      "@odata.type": "microsoft.graph.accessReviewReviewerScope"
    }
  ],
  "id": "String (identifier)",
  "reviewers": [
    {
      "@odata.type": "microsoft.graph.accessReviewReviewerScope"
    }
  ],
  "startDateTime": "String (timestamp)",
  
  "status": "String"
  
}
```

