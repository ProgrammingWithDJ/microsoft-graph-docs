---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAttachment()
name := "smile"
requestBody.SetName(&name) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.fileAttachment", 
	"contentBytes" : "R0lGODdhEAYEAA7", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Me().MessagesById("message-id").Attachments().Post(requestBody)


```