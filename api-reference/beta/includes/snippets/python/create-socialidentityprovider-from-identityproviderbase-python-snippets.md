---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = SocialIdentityProvider(
	odata_type = "microsoft.graph.socialIdentityProvider",
	display_name = "Login with Amazon",
	identity_provider_type = "Amazon",
	client_id = "56433757-cadd-4135-8431-2c9e3fd68ae8",
	client_secret = "000000000000",
)

result = await graph_client.identity.identity_providers.post(body = request_body)


```