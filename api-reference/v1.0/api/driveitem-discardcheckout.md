---
title: "driveItem: discardCheckout"
description: "Discard a previously checked out driveItem."
author: "javieralvarezchiang"
ms.localizationpriority: medium
ms.subservice: "sharepoint"
doc_type: apiPageType
ms.date: 12/10/2024
---

# driveItem: discardCheckout

Namespace: microsoft.graph


Discard the check out of a [driveItem](../resources/driveitem.md). This action releases a **driveItem** resource that was previously [checked out](driveitem-checkout.md). Any changes made to the item while it was checked out are discarded. 

The same user that performed the checkout must discard it. Another alternative is to use application permissions.


[!INCLUDE [national-cloud-support](../../includes/global-china.md)]

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).


<!-- {
  "blockType": "permissions",
  "name": "driveitem-discardcheckout-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/driveitem-discardcheckout-permissions.md)]

[!INCLUDE [app-permissions](../includes/sharepoint-embedded-app-driveitem-permissions.md)]

## HTTP request

``` http
POST /drive/root/discardCheckout
POST /drives/{drivesId}/root/discardCheckout
POST /shares/{sharesId}/root/discardCheckout
POST /drive/items/{driveItemId}/discardCheckout
POST /shares/{sharesId}/driveItem/discardCheckout
POST /drive/bundles/{driveItemId}/discardCheckout
POST /drive/special/{driveItemId}/discardCheckout
POST /drive/following/{driveItemId}/discardCheckout
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Request body

Don't supply a request body for this method.

## Response

If successful, this action returns a `204 No Content` response code.

The request returns `400 Bad Request` if the file isn't checked out. Requests made with delegated access return `423 Locked` if another user has the file checked out. Requests made with application access can discard any checkout. 

For more information about how errors are returned, see [Error responses][error-response].

## Examples

### Request

The following example shows a discard checkout request on a file identified by `{item-id}`.
<!-- {
  "blockType": "request",
  "name": "driveitemthis.discardcheckout"
}
-->
``` http
POST https://graph.microsoft.com/v1.0/drives/{drive-id}/items/{item-id}/discardCheckout
```

---



### Response

The following example shows the response.

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No content
```

[error-response]: /graph/errors
