---
title: "Update appManagementPolicy"
description: "Update an application management policy."
ms.localizationpriority: medium
author: "madansr7"
ms.prod: "identity-and-sign-in"
doc_type: "apiPageType"
---

# Update appManagementPolicy

Namespace: microsoft.graph

Update an [appManagementPolicy](../resources/appManagementPolicy.md) object.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
| :------------------------------------- | :------------------------------------------ |
| Delegated (work or school account)     | Policy.ReadWrite.ApplicationConfiguration   |
| Delegated (personal Microsoft account) | Not supported.                              |
| Application                            | Policy.ReadWrite.ApplicationConfiguration   |

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
PATCH /policies/appManagementPolicies/{id}
```

## Request headers

| Name          | Description                 |
| :------------ | :-------------------------- |
| Authorization | Bearer {token}. Required.   |
| Content-Type  | application/json. Required. |

## Request body

[!INCLUDE [table-intro](../../includes/update-property-table-intro.md)]

| Property     | Type                                                                     | Description                                                                              |
| :----------- | :----------------------------------------------------------------------- | :--------------------------------------------------------------------------------------- |
| displayName  | String                                                                   | The display name of the policy. Inherited from [policyBase](../resources/policybase.md). |
| description  | String                                                                   | The description of the policy. Inherited from [policyBase](../resources/policybase.md).  |
| isEnabled    | Boolean                                                                  | Denotes whether the policy is enabled.                                                   |
| restrictions | [appManagementConfiguration](../resources/appManagementConfiguration.md) | Restrictions that apply to an application or service principal object.                   |

## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request

The following is an example of the request.

<!-- {
  "blockType": "request",
  "name": "update_appManagementPolicy"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/policies/appManagementPolicies/{id}

{
    "isEnabled": false
}

```

### Response

The following is an example of the response.

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content

```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "update appManagementPolicies",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
