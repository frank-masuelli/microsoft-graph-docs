---
title: "Update browserSharedCookie"
description: "Update the properties of a browserSharedCookie object."
author: "edward-day-vii"
ms.localizationpriority: medium
ms.prod: "browser-management"
doc_type: apiPageType
---

# Update browserSharedCookie
Namespace: microsoft.graph

Update the properties of a [browserSharedCookie](../resources/browsersharedcookie.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "browsersharedcookie_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/browsersharedcookie-update-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /admin/edge/internetExplorerMode/siteLists/{browserSiteListId}/sharedCookies/{browserSharedCookieId}
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
|comment|String|The comment of the cookie.|
|displayName|String|The name of the cookie.|
|hostOnly|Boolean|Determines whether a cookie is a host-only or domain cookie.|
|hostOrDomain|String|The URL of the cookie.|
|path|String|The path of the cookie.|
|sourceEnvironment|browserSharedCookieSourceEnvironment|Specifies how the cookies are shared between Microsoft Edge and Internet Explorer. The possible values are: `microsoftEdge`, `internetExplorer11`, `both`, `unknownFutureValue`.|


## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request
The following is an example of a request.
<!-- {
  "blockType": "request",
  "name": "update_browsersharedcookie",
  "sampleKeys": ["20579923-e6c8-425a-b728-47f43c10bc05", "972a5778-df43-45fd-9c2a-5dd944c7a1ce"]
}
-->
``` http
PATCH https://graph.microsoft.com/v1.0/admin/edge/internetExplorerMode/siteLists/20579923-e6c8-425a-b728-47f43c10bc05/sharedCookies/972a5778-df43-45fd-9c2a-5dd944c7a1ce
Content-Type: application/json
Content-length: 349

{
  "hostOrDomain": "www.microsoft.com",
  "sourceEnvironment": "microsoftEdge",
  "displayName": "Microsoft Cookie",
  "path": "/",
  "hostOnly": true,
  "comment": "Updating source environment."
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

