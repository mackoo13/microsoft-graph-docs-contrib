---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = UpgradePostRequestBody(
)

await graph_client.chats.by_chat_id('chat-id').installed_apps.by_installed_app_id('teamsAppInstallation-id').upgrade.post(body = request_body)


```