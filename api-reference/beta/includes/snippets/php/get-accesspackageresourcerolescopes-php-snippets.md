---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestConfiguration = new AccessPackageRequestBuilderGetRequestConfiguration();

$queryParameters = new AccessPackageRequestBuilderGetQueryParameters();
$queryParameters->expand = ["accessPackageResourceRoleScopes($expand=accessPackageResourceRole,accessPackageResourceScope)"];

$requestConfiguration->queryParameters = $queryParameters;


$requestResult = $graphServiceClient->identityGovernance()->entitlementManagement()->accessPackagesById('accessPackage-id')->get($requestConfiguration);


```