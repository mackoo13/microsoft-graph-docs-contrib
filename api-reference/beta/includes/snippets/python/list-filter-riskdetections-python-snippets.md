---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

query_params = RiskDetectionsRequestBuilder.RiskDetectionsRequestBuilderGetQueryParameters(
		filter = "riskEventType eq 'unfamiliarFeatures' or riskLevel eq 'medium'",
)

request_configuration = RiskDetectionsRequestBuilder.RiskDetectionsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.identity_protection.risk_detections.get(request_configuration = request_configuration)


```