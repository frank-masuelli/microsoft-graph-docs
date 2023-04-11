---
title: "Delete browserSiteList"
description: "Delete a browserSiteList object."
author: "edward-day-vii"
ms.localizationpriority: medium
ms.prod: "browser-management"
doc_type: apiPageType
---

# Delete browserSiteList
Namespace: microsoft.graph

Delete a [browserSiteList](../resources/browsersitelist.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "internetexplorermode_delete_sitelists" } -->
[!INCLUDE [permissions-table](../includes/permissions/internetexplorermode-delete-sitelists-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /admin/edge/internetExplorerMode/siteLists/{browserSiteListId}
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
  "name": "delete_browsersitelist",
  "sampleKeys": ["36ba61eb-c492-4283-a38b-963a1dbb2f69"]
}
-->
``` http
DELETE https://graph.microsoft.com/v1.0/admin/edge/internetExplorerMode/siteLists/36ba61eb-c492-4283-a38b-963a1dbb2f69
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

