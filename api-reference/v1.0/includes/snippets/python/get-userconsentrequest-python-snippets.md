---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)


result = await graph_client.identity_governance.app_consent.app_consent_requests.by_app_consent_request_id('appConsentRequest-id').user_consent_requests.by_user_consent_request_id('userConsentRequest-id').get()


```