---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestConfiguration = new UnifiedRoleDefinitionRequestBuilderGetRequestConfiguration();

$queryParameters = new UnifiedRoleDefinitionRequestBuilderGetQueryParameters();
$queryParameters->expand = ["inheritsPermissionsFrom"];

$requestConfiguration->queryParameters = $queryParameters;


$requestResult = $graphServiceClient->roleManagement()->directory()->roleDefinitionsById('unifiedRoleDefinition-id')->get($requestConfiguration);


```