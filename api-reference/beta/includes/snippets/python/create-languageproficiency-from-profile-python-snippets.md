---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = LanguageProficiency(
	display_name = "Norwegian Bokmål",
	tag = "nb-NO",
	spoken = LanguageProficiencyLevel.NativeOrBilingual,
	written = LanguageProficiencyLevel.NativeOrBilingual,
	reading = LanguageProficiencyLevel.NativeOrBilingual,
)

result = await graph_client.me.profile.languages.post(body = request_body)


```