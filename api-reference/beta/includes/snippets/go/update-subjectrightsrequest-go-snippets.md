---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewSubjectRightsRequest()
internalDueDateTime , err := time.Parse(time.RFC3339, "2021-08-30T00:00:00Z")
requestBody.SetInternalDueDateTime(&internalDueDateTime) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.subjectRightsRequest", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.Privacy().SubjectRightsRequestsById("subjectRightsRequest-id").Patch(requestBody)


```