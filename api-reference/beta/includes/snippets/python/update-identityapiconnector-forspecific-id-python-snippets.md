---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = IdentityApiConnector(
	authentication_configuration = Pkcs12Certificate(
		odata_type = "#microsoft.graph.pkcs12Certificate",
		pkcs12_value = "eyJhbGciOiJSU0EtT0FFUCIsImVuYyI6IkEyNTZHQ00ifQ...kDJ04sJShkkgjL9Bm49plA",
		password = "secret",
	),
)

result = await graph_client.identity.api_connectors.by_api_connector_id('identityApiConnector-id').patch(body = request_body)


```