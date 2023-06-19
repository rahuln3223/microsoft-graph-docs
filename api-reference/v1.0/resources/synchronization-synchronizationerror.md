---
title: "synchronizationError resource type"
description: "Represents an error that occurred during the synchronization process."
ms.localizationpriority: medium
doc_type: resourcePageType
author: "ArvindHarinder1"
ms.prod: "applications"
---

# synchronizationError resource type

Namespace: microsoft.graph

Represents an error that occurred during the synchronization process.

## Properties

<!-- Add descriptions for the properties. Fill in the examples. -->
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|code|String| The error code. |
|message|String| The error message.  |
|tenantActionable|Boolean| The action to take to resolve the error.|

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationError"
}-->

```json
{
  "code": "String",
  "message": "String",
  "tenantActionable": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "synchronizationError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


