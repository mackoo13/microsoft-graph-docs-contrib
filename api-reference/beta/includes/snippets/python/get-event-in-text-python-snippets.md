---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

query_params = EventRequestBuilder.EventRequestBuilderGetQueryParameters(
		select = ["subject","body","bodyPreview"],
)

request_configuration = EventRequestBuilder.EventRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
headers = {
			'Prefer' : "outlook.body-content-type=\"text\"",
}

)

result = await graph_client.me.events.by_event_id('event-id').get(request_configuration = request_configuration)


```