---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = DeviceComplianceSettingState(
	odata_type = "#microsoft.graph.deviceComplianceSettingState",
	setting = "Setting value",
	setting_name = "Setting Name value",
	device_id = "Device Id value",
	device_name = "Device Name value",
	user_id = "User Id value",
	user_email = "User Email value",
	user_name = "User Name value",
	user_principal_name = "User Principal Name value",
	device_model = "Device Model value",
	state = ComplianceStatus.NotApplicable,
	compliance_grace_period_expiration_date_time = "2016-12-31T23:56:44.951111-08:00",
)

result = await graph_client.device_management.device_compliance_policy_setting_state_summaries.by_device_compliance_policy_setting_state_summarie_id('deviceCompliancePolicySettingStateSummary-id').device_compliance_setting_states.by_device_compliance_setting_state_id('deviceComplianceSettingState-id').patch(body = request_body)


```