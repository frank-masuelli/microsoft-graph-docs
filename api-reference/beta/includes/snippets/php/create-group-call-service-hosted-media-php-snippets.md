---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new Call();
$requestBody->set@odatatype('#microsoft.graph.call');

$requestBody->setDirection(new CallDirection('outgoing'));

$requestBody->setSubject('Create a group call with service hosted media');

$requestBody->setCallbackUri('https://bot.contoso.com/callback');

$source = new ParticipantInfo();
$sourceIdentity = new IdentitySet();
$sourceIdentity->set@odatatype('#microsoft.graph.identitySet');

$sourceIdentityApplication = new Identity();
$sourceIdentityApplication->set@odatatype('#microsoft.graph.identity');

$sourceIdentityApplication->setDisplayName('TestBot');

$sourceIdentityApplication->setId('dd3885da-f9ab-486b-bfae-85de3d445555');


$sourceIdentity->setApplication($sourceIdentityApplication);

$source->setIdentity($sourceIdentity);
$additionalData = [
'@odata.type' => '#microsoft.graph.participantInfo', 
];
$source->setAdditionalData($additionalData);



$requestBody->setSource($source);
$targetsInvitationParticipantInfo1 = new InvitationParticipantInfo();
$targetsInvitationParticipantInfo1Identity = new IdentitySet();
$targetsInvitationParticipantInfo1Identity->set@odatatype('#microsoft.graph.identitySet');

$targetsInvitationParticipantInfo1IdentityUser = new Identity();
$targetsInvitationParticipantInfo1IdentityUser->set@odatatype('#microsoft.graph.identity');

$targetsInvitationParticipantInfo1IdentityUser->setDisplayName('user1');

$targetsInvitationParticipantInfo1IdentityUser->setId('98da8a1a-1b87-452c-a713-65d3f10b5555');


$targetsInvitationParticipantInfo1Identity->setUser($targetsInvitationParticipantInfo1IdentityUser);

$targetsInvitationParticipantInfo1->setIdentity($targetsInvitationParticipantInfo1Identity);
$additionalData = [
'@odata.type' => '#microsoft.graph.invitationParticipantInfo', 
];
$targetsInvitationParticipantInfo1->setAdditionalData($additionalData);



$targetsArray []= $targetsInvitationParticipantInfo1;
$targetsInvitationParticipantInfo2 = new InvitationParticipantInfo();
$targetsInvitationParticipantInfo2Identity = new IdentitySet();
$targetsInvitationParticipantInfo2Identity->set@odatatype('#microsoft.graph.identitySet');

$targetsInvitationParticipantInfo2IdentityUser = new Identity();
$targetsInvitationParticipantInfo2IdentityUser->set@odatatype('#microsoft.graph.identity');

$targetsInvitationParticipantInfo2IdentityUser->setDisplayName('user2');

$targetsInvitationParticipantInfo2IdentityUser->setId('bf5aae9a-d11d-47a8-93b1-782504c95555');


$targetsInvitationParticipantInfo2Identity->setUser($targetsInvitationParticipantInfo2IdentityUser);

$targetsInvitationParticipantInfo2->setIdentity($targetsInvitationParticipantInfo2Identity);
$additionalData = [
'@odata.type' => '#microsoft.graph.participantInfo', 
];
$targetsInvitationParticipantInfo2->setAdditionalData($additionalData);



$targetsArray []= $targetsInvitationParticipantInfo2;
$requestBody->setTargets($targetsArray);


$requestBody->setRequestedModalities(['audio', ]);

$mediaConfig = new MediaConfig();
$mediaConfig->set@odatatype('#microsoft.graph.serviceHostedMediaConfig');

$mediaConfig->setRemoveFromDefaultAudioGroup(false);


$requestBody->setMediaConfig($mediaConfig);
$requestBody->setTenantId('aa67bd4c-8475-432d-bd41-39f255720e0a');



$requestResult = $graphServiceClient->communications()->calls()->post($requestBody);


```