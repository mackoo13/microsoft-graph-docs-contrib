---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = DelegatedAdminRelationship(
	display_name = "Updated Contoso admin relationship",
	duration = "P31D",
	customer = DelegatedAdminRelationshipCustomerParticipant(
		tenant_id = "52eaad04-13a2-4a2f-9ce8-93a294fadf36",
	),
	access_details = DelegatedAdminAccessDetails(
		unified_roles = [
			UnifiedRole(
				role_definition_id = "44367163-eba1-44c3-98af-f5787879f96a",
			),
			UnifiedRole(
				role_definition_id = "29232cdf-9323-42fd-ade2-1d097af3e4de",
			),
			UnifiedRole(
				role_definition_id = "69091246-20e8-4a56-aa4d-066075b2a7a8",
			),
			UnifiedRole(
				role_definition_id = "3a2c62db-5318-420d-8d74-23affee5d9d5",
			),
		]
	),
)

request_configuration = DelegatedAdminRelationshipRequestBuilder.DelegatedAdminRelationshipRequestBuilderPatchRequestConfiguration(
headers = {
		'If-Match' : "W/\"JyI0NzAwNjg0NS0wMDAwLTE5MDAtMDAwMC02MGY0Yjg4MzAwMDAiJw==\"",
}

)

result = await graph_client.tenant_relationships.delegated_admin_relationships.by_delegated_admin_relationship_id('delegatedAdminRelationship-id').patch(body = request_body, request_configuration = request_configuration)


```