---
title: "hardwareOathAuthenticationMethod: deactivate"
description: "Deactive a hardware OATH token. It remains assigned to a user."
author: "luc-msft"
ms.localizationpriority: medium
ms.subservice: "entra-sign-in"
doc_type: apiPageType
ms.date: 12/06/2024
---

# hardwareOathAuthenticationMethod: deactivate

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Deactive a [hardware OATH token](../resources/hardwareoathauthenticationmethod.md). It remains assigned to a user.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

## Permissions acting on self
<!-- {
  "blockType": "permissions",
  "name": "hardwareoathauthenticationmethod-deactivate-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/hardwareoathauthenticationmethod-deactivate-permissions.md)]

## Permissions acting on another user
<!-- {
  "blockType": "permissions",
  "name": "hardwareoathauthenticationmethod-deactivate-2-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/hardwareoathauthenticationmethod-deactivate-2-permissions.md)]

## HTTP request
Deactivate a hardware OATH authentication method assigned to you.
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /me/authentication/hardwareOathMethods/{hardwareOathAuthenticationMethodId}/deactivate
```

Deactivate a hardware OATH authentication method assigned to another user.
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/authentication/hardwareOathMethods/{hardwareOathAuthenticationMethodId}/deactivate
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Request body

Don't supply a request body for this method.

## Response

If successful, this action returns a `204 No Content` response code.

## Examples

### Request

The following example shows a request.
# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "hardwareoathauthenticationmethodthis.deactivate"
}
-->
``` http
POST https://graph.microsoft.com/beta/me/authentication/hardwareOathMethods/{hardwareOathAuthenticationMethodId}/deactivate
```

# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/hardwareoathauthenticationmethodthisdeactivate-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [CLI](#tab/cli)
[!INCLUDE [sample-code](../includes/snippets/cli/hardwareoathauthenticationmethodthisdeactivate-cli-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/hardwareoathauthenticationmethodthisdeactivate-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/hardwareoathauthenticationmethodthisdeactivate-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/hardwareoathauthenticationmethodthisdeactivate-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [PHP](#tab/php)
[!INCLUDE [sample-code](../includes/snippets/php/hardwareoathauthenticationmethodthisdeactivate-php-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Python](#tab/python)
[!INCLUDE [sample-code](../includes/snippets/python/hardwareoathauthenticationmethodthisdeactivate-python-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### Response

The following example shows the response.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```

