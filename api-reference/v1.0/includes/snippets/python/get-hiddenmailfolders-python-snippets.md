---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

query_params = MailFoldersRequestBuilder.MailFoldersRequestBuilderGetQueryParameters(
		include_hidden_folders = "true",
)

request_configuration = MailFoldersRequestBuilder.MailFoldersRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.me.mail_folders.get(request_configuration = request_configuration)


```