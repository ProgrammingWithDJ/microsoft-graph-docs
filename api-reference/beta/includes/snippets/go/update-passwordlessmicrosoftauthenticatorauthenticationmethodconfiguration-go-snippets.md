---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAuthenticationMethodConfiguration()
state := graphmodels.ENABLED_AUTHENTICATIONMETHODSTATE 
requestBody.SetState(&state) 
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.passwordlessMicrosoftAuthenticatorAuthenticationMethodConfiguration", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.Policies().AuthenticationMethodsPolicy().AuthenticationMethodConfigurationsById("authenticationMethodConfiguration-id").Patch(requestBody)


```