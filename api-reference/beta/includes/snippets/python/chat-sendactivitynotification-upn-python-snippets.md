---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = SendActivityNotificationPostRequestBody(
	topic = TeamworkActivityTopic(
		source = TeamworkActivityTopicSource.EntityUrl,
		value = "https://graph.microsoft.com/beta/chats/{chatId}/messages/{messageId}",
	),
	activity_type = "approvalRequired",
	preview_text = ItemBody(
		content = "Deployment requires your approval",
	),
	recipient = AadUserNotificationRecipient(
		odata_type = "microsoft.graph.aadUserNotificationRecipient",
		user_id = "jacob@contoso.com",
	),
	template_parameters = [
		KeyValuePair(
			name = "approvalTaskId",
			value = "2020AAGGTAPP",
		),
	]
)

await graph_client.chats.by_chat_id('chat-id').send_activity_notification.post(body = request_body)


```