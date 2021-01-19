---
title: "estimateStatisticsOperation resource type"
description: "The operation that handles estimating the count and size of a collection"
author: "mahage-msft"
localization_priority: Normal
ms.prod: "ediscovery"
doc_type: resourcePageType
---

# estimateStatisticsOperation resource type

Namespace: microsoft.graph

The operation that handles estimating the count and size of a [sourceCollection](../resources/sourcecollection.md). See [Collect data for a case in Advanced eDiscovery](https://docs.microsoft.com/microsoft-365/compliance/collecting-data-for-ediscovery) to learn more.

Inherits from [caseOperation](../resources/caseoperation.md).

## Methods

None

## Properties

|Property|Type|Description|
|:---|:---|:---|
|action|caseAction| The type of operation - `estimateStatistics`. Read-only. Inherited from [caseOperation](../resources/caseoperation.md).|
|completedDateTime|DateTimeOffset|The date and time the operation was completed. Read-only. Inherited from [caseOperation](../resources/caseoperation.md)|
|createdBy|[identitySet](../resources/identityset.md)|The user who created the operation. Read-only. Inherited from [caseOperation](../resources/caseoperation.md)|
|createdDateTime|DateTimeOffset|The date and time the operation was started. Read-only. Inherited from [caseOperation](../resources/caseoperation.md)|
|id|String| The ID for the operation. Read-only. Inherited from [caseOperation](../resources/caseoperation.md).|
|indexedItemCount|Int64|The estimated count of items for the **sourceCollection** that matched the contentQuery.|
|indexedItemsSize|Int64|The estimated size of items for the **sourceCollection** that matched the contentQuery.|
|mailboxCount|Int32|The number of mailboxes that had search hits.|
|percentProgress|Int32|The progress of the operation. Read-only. Inherited from [caseOperation](../resources/caseoperation.md)|
|resultInfo|[resultInfo](../resources/resultinfo.md)|Contains success and failure-specific result information. Inherited from [caseOperation](../resources/caseoperation.md)|
|siteCount|Int32|The number of mailboxes that had search hits.|
|status|caseOperationStatus|The status of the case operation. Inherited from [caseOperation](../resources/caseoperation.md). Possible values are: `notStarted`, `submissionFailed`, `running`, `succeeded`, `partiallySucceeded`, `failed`.|
|unindexedItemCount|Int64|The estimated count of unindexed items for the collection.|
|unindexedItemsSize|Int64|The estimated size of unindexed items for the collection.|

## Relationships

|Relationship|Type|Description|
|:---|:---|:---|
|sourceCollection|[sourceCollection](../resources/sourcecollection.md)|**TODO: Add Description**|

## JSON representation

The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.estimateStatisticsOperation",
  "baseType": "microsoft.graph.caseOperation",
  "openType": false
}
-->

``` json
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#compliance/ediscovery/cases/47746044-fd0b-4a30-acfc-5272b691ba5b/operations/$entity",
    "@odata.type": "#microsoft.graph.estimateStatisticsOperation",
    "createdDateTime": "2021-01-12T18:47:23.3974907Z",
    "completedDateTime": "2021-01-12T18:47:51.1461805Z",
    "percentProgress": 100,
    "status": "succeeded",
    "action": "estimateStatistics",
    "id": "82edd40e182a464fa02c24a36fa94873",
    "indexedItemCount": 2,
    "indexedItemsSize": 39276,
    "unindexedItemCount": 0,
    "unindexedItemsSize": 0,
    "mailboxCount": 1,
    "siteCount": 0,
    "createdBy": {
        "user": {
            "id": "c1db6f13-332a-4d84-b111-914383ff9fc9",
            "displayName": null,
            "userPrincipalName": "admin@contoso.com"
        }
    }
}
```