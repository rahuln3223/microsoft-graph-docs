---
title: "Restore deleted item (directory object)"
description: "Restore a recently deleted application, group, service principal, or user from deleted items."
author: "keylimesoda"
ms.localizationpriority: medium
ms.prod: "directory-management"
doc_type: apiPageType
---

# Restore deleted item (directory object)

Namespace: microsoft.graph

Restore a recently deleted [application](../resources/application.md), [group](../resources/group.md), [servicePrincipal](../resources/serviceprincipal.md), [administrative unit](../resources/administrativeunit.md), or [user](../resources/user.md) object from [deleted items](../resources/directory.md). If an item was accidentally deleted, you can fully restore the item. This is not applicable to security groups, which are deleted permanently.

A recently deleted item will remain available for up to 30 days. After 30 days, the item is permanently deleted.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

### For applications and service principals:

<!-- { "blockType": "permissions", "name": "directory_deleteditems_restore" } -->
[!INCLUDE [permissions-table](../includes/permissions/directory-deleteditems-restore-permissions.md)]

The calling app must be assigned one of the following [Azure AD roles](/azure/active-directory/roles/permissions-reference):
+ Global Administrator
+ Application Administrator
+ Cloud Application Administrator
+ Hybrid Identity Administrator

### For users:

<!-- { "blockType": "permissions", "name": "directory_deleteditems_restore_2" } -->
[!INCLUDE [permissions-table](../includes/permissions/directory-deleteditems-restore-2-permissions.md)]

To restore users with privileged administrator roles in delegated scenarios, the app must be assigned with *Directory.AccessAsUser.All* delegated permission, and the calling user must also be assigned a higher privileged administrator role as indicated in [Who can perform sensitive actions](../resources/users.md#who-can-perform-sensitive-actions).

In app-only scenarios, the *User.ReadWrite.All* application permission isn't enough privilege to restore deleted users with privilged administrator roles. The app must be assigned a higher privileged administrator role as indicated in [Who can perform sensitive actions](../resources/users.md#who-can-perform-sensitive-actions).

### For groups:

<!-- { "blockType": "permissions", "name": "directory_deleteditems_restore_3" } -->
[!INCLUDE [permissions-table](../includes/permissions/directory-deleteditems-restore-3-permissions.md)]

### For administrative units:

<!-- { "blockType": "permissions", "name": "directory_deleteditems_restore_4" } -->
[!INCLUDE [permissions-table](../includes/permissions/directory-deleteditems-restore-4-permissions.md)]


## HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /directory/deletedItems/{id}/restore
```

## Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer &lt;token&gt; *Required*|
| Content-type | application/json |

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [directoryObject](../resources/directoryobject.md) object in the response body.

## Example
### Request


# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "restore_directory_deleteditem"
}-->
```http
POST https://graph.microsoft.com/v1.0/directory/deletedItems/{object-id}/restore
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/restore-directory-deleteditem-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/restore-directory-deleteditem-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/restore-directory-deleteditem-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/restore-directory-deleteditem-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PowerShell](#tab/powershell)
[!INCLUDE [sample-code](../includes/snippets/powershell/restore-directory-deleteditem-powershell-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/restore-directory-deleteditem-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### Response
Note: The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#directoryObjects/$entity",
  "@odata.type":"#microsoft.graph.group",
  "id":"46cc6179-19d0-473e-97ad-6ff84347bbbb",
  "displayName":"SampleGroup",
  "groupTypes":["Unified"],
  "mail":"example@contoso.com",
  "mailEnabled":true,
  "mailNickname":"Example",
  "securityEnabled":false,
  "visibility":"Public"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create deletedItem",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->

