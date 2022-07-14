---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestConfiguration = new TeamsAppsRequestBuilderGetRequestConfiguration();

$queryParameters = new TeamsAppsRequestBuilderGetQueryParameters();
$queryParameters->expand = ["appDefinitions($expand=bot)"];
$queryParameters->filter = "appDefinitions/any";

$requestConfiguration->queryParameters = $queryParameters;


$requestResult = $graphServiceClient->appCatalogs()->teamsApps()->get($requestConfiguration);


```