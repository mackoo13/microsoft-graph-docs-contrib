---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = FederatedIdentityCredential(
	name = "testing02",
	issuer = "https://login.microsoftonline.com/3d1e2be9-a10a-4a0c-8380-7ce190f98ed9/v2.0",
	subject = "a7d388c3-5e3f-4959-ac7d-786b3383006a",
	audiences = [
		"api://AzureADTokenExchange",
	]
)

result = await graph_client.applications.by_application_id('application-id').federated_identity_credentials.post(body = request_body)


```