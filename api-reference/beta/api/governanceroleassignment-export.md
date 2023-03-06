---
title: "Export governanceRoleAssignmentRequests"
description: "Retrieve a collection of governanceRoleAssignmentRequests in the format `application/octet-stream`, which can be parsed as a .csv file in the browser."
ms.localizationpriority: medium
doc_type: apiPageType
ms.prod: "governance"
author: "rkarim-ms"
---

# Export governanceRoleAssignmentRequests

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

[!INCLUDE [pim-v2ResourceRoles-deprecation](../../includes/pim-v2ResourceRoles-deprecation.md)]

Retrieve a collection of [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) in the format `application/octet-stream`, which can be parsed as a .csv file in the browser.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference#privileged-access-permissions).

### Azure resources

<!-- { "blockType": "permissions", "name": "governanceroleassignment_export" } -->
[!INCLUDE [permissions-table](../includes/permissions/governanceroleassignment-export-permissions.md)]

### Azure AD

<!-- { "blockType": "permissions", "name": "governanceroleassignment_export_2" } -->
[!INCLUDE [permissions-table](../includes/permissions/governanceroleassignment-export-2-permissions.md)]

### Groups

<!-- { "blockType": "permissions", "name": "governanceroleassignment_export_3" } -->
[!INCLUDE [permissions-table](../includes/permissions/governanceroleassignment-export-3-permissions.md)]


## HTTP request
<!-- { "blockType": "ignored" } -->
Export a collection of [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) on a resource
    
>**Note:** Besides the permission scope, this request requires the requestor to have at least one role assignment on the resource. 
    
```http
GET /privilegedAccess/azureResources/roleAssignments/export?$filter=resourceId+eq+'{resourceId}'
```

Export a collection of [governanceRoleAssignmentRequests](../resources/governanceroleassignmentrequest.md) of mine
```http
GET /privilegedAccess/azureResources/roleAssignments/export?$filter=subjectId+eq+'{myId}'
```
## Optional query parameters
This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.

## Request headers
| Name      |Description|
|:----------|:----------|
| Authorization  | Bearer {code}|

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and content of type `application/octet-stream`.

## Example
This example saves all role assignments as a .csv file in the subscription Wingtip Toys - Prod. 

##### Request
```http
GET https://graph.microsoft.com/beta/privilegedAccess/azureResources/roleAssignments/export?filter=resourceId+eq+'85dfe48a-55d3-49fc-8f36-ee14b7f6f720'
```
##### Response
Here is an example of the response. 
```http
HTTP/1.1 200 OK
Content-Type:application/octet-stream
Content-Length:126

77u/77u/QXNzaWdubWVudCBMZXZlbCxVc2VyIEdyb3VwIE5hbWUsUm9sZSBOYW1lLEVtYWlsLEFzc2lnbm1lbnQgVHlwZSxBc3NpZ25tZW43IFN0YXJ0IFRpbWUgKFVUQyksQXNzaWdubWVudCBFbmQgVGltZdAoVVRDKQ0K

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Export governanceRoleAssignmentRequests",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


