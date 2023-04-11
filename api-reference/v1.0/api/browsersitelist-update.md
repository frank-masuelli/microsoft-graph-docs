---
title: "Update browserSiteList"
description: "Update the properties of a browserSiteList object."
author: "edward-day-vii"
ms.localizationpriority: medium
ms.prod: "browser-management"
doc_type: apiPageType
---

# Update browserSiteList
Namespace: microsoft.graph

Update the properties of a [browserSiteList](../resources/browsersitelist.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "browsersitelist_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/browsersitelist-update-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /admin/edge/internetExplorerMode/siteLists/{browserSiteListId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
[!INCLUDE [table-intro](../../includes/update-property-table-intro.md)]


|Property|Type|Description|
|:---|:---|:---|
|description|String|Description for the site list.|
|displayName|String|Display name of this site list.|



## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request
The following is an example of a request.
<!-- {
  "blockType": "request",
  "name": "update_browsersitelist",
  "sampleKeys": ["36ba61eb-c492-4283-a38b-963a1dbb2f69"]
}
-->
``` http
PATCH https://graph.microsoft.com/v1.0/admin/edge/internetExplorerMode/siteLists/36ba61eb-c492-4283-a38b-963a1dbb2f69
Content-Type: application/json
Content-length: 283

{
    "displayName": "Production Site List A",
    "description": "Production site list for team A"
}
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

