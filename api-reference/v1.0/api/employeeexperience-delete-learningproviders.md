---
title: "Delete learningProvider"
description: "Delete a learningProvider resource and remove its registration in Viva Learning for a tenant."
author: "malabikaroy"
ms.localizationpriority: medium
ms.prod: "employee-learning"
doc_type: apiPageType
---

# Delete learningProvider

Namespace: microsoft.graph

Delete a [learningProvider](../resources/learningprovider.md) resource and remove its registration in Viva Learning for a tenant.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "employeeexperience_delete_learningproviders" } -->
[!INCLUDE [permissions-table](../includes/permissions/employeeexperience-delete-learningproviders-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /employeeExperience/learningProviders/{learningProviderId}/$ref
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request

The following is an example of a request.
<!-- {
  "blockType": "request",
  "name": "delete_learningprovider"
}
-->
``` http
DELETE https://graph.microsoft.com/v1.0/employeeExperience/learningProviders/13727311-e7bb-470d-8b20-6a23d9030d70/$ref
```

### Response

The following is an example of the response.

<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```
