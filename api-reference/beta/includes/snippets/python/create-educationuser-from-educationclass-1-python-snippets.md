---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ReferenceCreate(
	odata_id = "https://graph.microsoft.com/beta/education/users/13015",
)

await graph_client.education.classes.by_classe_id('educationClass-id').members.ref.post(body = request_body)


```