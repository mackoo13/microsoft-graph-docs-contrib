---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

// Code snippets are only available for the latest version. Current version is 5.x

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new Microsoft.Graph.DirectoryObjects.GetAvailableExtensionProperties.GetAvailableExtensionPropertiesPostRequestBody
{
};
var result = await graphClient.DirectoryObjects.GetAvailableExtensionProperties.PostAsync(requestBody);


```