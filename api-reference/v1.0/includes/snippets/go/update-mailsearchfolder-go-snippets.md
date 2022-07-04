---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewMailFolder()
additionalData := map[string]interface{}{
	"@odata.type" : "microsoft.graph.mailSearchFolder", 
	"filterQuery" : "contains(subject, 'Analytics')", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.Me().MailFoldersById("mailFolder-id").Patch(requestBody)


```