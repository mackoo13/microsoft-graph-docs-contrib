---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

query_params = FilterByCurrentUserWithOnRequestBuilder.FilterByCurrentUserWithOnRequestBuilderGetQueryParameters(
		expand = ["instance($expand=definition)"],
)

request_configuration = FilterByCurrentUserWithOnRequestBuilder.FilterByCurrentUserWithOnRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.identity_governance.acce_reviews.decisions.filter_by_current_user(on='{on}'.get(request_configuration = request_configuration)


```