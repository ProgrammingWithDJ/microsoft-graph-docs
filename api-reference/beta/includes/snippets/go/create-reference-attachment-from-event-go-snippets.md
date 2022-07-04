---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAttachment()
name := "Personal pictures"
requestBody.SetName(&name) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.referenceAttachment", 
	"sourceUrl" : "https://contoso.com/personal/mario_contoso_net/Documents/Pics", 
	"providerType" : "oneDriveConsumer", 
	"permission" : "Edit", 
	"isFolder" : "True", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Me().EventsById("event-id").Attachments().Post(requestBody)


```