---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new CertificateAuthorityAsEntity
{
	IsRootAuthority = true,
};
var result = await graphClient.Directory.CertificateAuthorities.CertificateBasedApplicationConfigurations["{certificateBasedApplicationConfiguration-id}"].TrustedCertificateAuthorities["{certificateAuthorityAsEntity-id}"].PatchAsync(requestBody);


```