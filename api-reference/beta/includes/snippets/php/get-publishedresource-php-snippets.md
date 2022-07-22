---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestConfiguration = new PublishedResourceRequestBuilderGetRequestConfiguration();

$queryParameters = new PublishedResourceRequestBuilderGetQueryParameters();
$queryParameters->expand = ["agentGroups"];

$requestConfiguration->queryParameters = $queryParameters;


$requestResult = $graphServiceClient->onPremisesPublishingProfilesById('onPremisesPublishingProfile-id')->publishedResourcesById('publishedResource-id')->get($requestConfiguration);


```