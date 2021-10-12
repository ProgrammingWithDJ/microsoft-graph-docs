---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var groups = await graphClient.Groups
	.Request()
	.Header("ConsistencyLevel","eventual")
	.Filter("mailEnabled eq false and securityEnabled eq true and NOT(groupTypes/any(s:s eq 'Unified')) and membershipRuleProcessingState eq 'On'")
	.Select("id,membershipRule,membershipRuleProcessingState")
	.GetAsync();

```