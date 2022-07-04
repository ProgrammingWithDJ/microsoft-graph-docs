---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewEducationAssignmentResource()
distributeForStudentWork := false
requestBody.SetDistributeForStudentWork(&distributeForStudentWork) 
resource := graphmodels.NewEducationResource()
displayName := "Where the Wonders of Learning Never Cease | Wonderopolis"
resource.SetDisplayName(&displayName) 
additionalData := map[string]interface{}{
	"link" : "https://wonderopolis.org/", 
	thumbnailPreviewUrl := null
resource.SetThumbnailPreviewUrl(&thumbnailPreviewUrl) 
	"@odata.type" : "#microsoft.graph.educationLinkResource", 
}
resource.SetAdditionalData(additionalData)
requestBody.SetResource(resource)

result, err := graphClient.Education().ClassesById("educationClass-id").AssignmentsById("educationAssignment-id").Resources().Post(requestBody)


```