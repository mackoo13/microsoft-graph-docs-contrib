---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = PublishedResource(
	display_name = "Demo provisioning (updated)",
)

result = await graph_client.on_premise_publishing_profiles.by_on_premise_publishing_profile_id('onPremisesPublishingProfile-id').published_resources.by_published_resource_id('publishedResource-id').patch(body = request_body)


```