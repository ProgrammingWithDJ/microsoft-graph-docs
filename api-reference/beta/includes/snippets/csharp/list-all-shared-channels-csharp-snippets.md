---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var channels = await graphClient.Teams["{team-id}"].AllChannels
	.Request()
	.Filter("membershipType eq 'shared'")
	.GetAsync();

```