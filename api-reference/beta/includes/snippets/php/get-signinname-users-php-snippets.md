---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestConfiguration = new UsersRequestBuilderGetRequestConfiguration();

$queryParameters = new UsersRequestBuilderGetQueryParameters();
$queryParameters->select = ["displayName","id"];
$queryParameters->filter = "identities/any";

$requestConfiguration->queryParameters = $queryParameters;


$requestResult = $graphServiceClient->users()->get($requestConfiguration);


```