---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = CloudPcExportJob(
	report_name = CloudPcReportName.TotalAggregatedRemoteConnectionReports,
	select = [
		"CloudPcId",
		"ManagedDeviceName",
		"UserPrincipalName",
		"DaysSinceLastSignIn",
		"TotalUsageInHour",
	]
)

result = await graph_client.device_management.virtual_endpoint.reports.export_jobs.post(body = request_body)


```