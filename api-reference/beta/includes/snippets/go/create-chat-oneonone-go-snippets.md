---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewChat()
chatType := graphmodels.ONEONONE_CHATTYPE 
requestBody.SetChatType(&chatType) 


conversationMember := graphmodels.NewConversationMember()
roles := []String {
	"owner",

}
conversationMember.SetRoles(roles)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.aadUserConversationMember", 
	"user@odata.bind" : "https://graph.microsoft.com/beta/users('8b081ef6-4792-4def-b2c9-c363a1bf41d5')", 
}
conversationMember.SetAdditionalData(additionalData)
conversationMember1 := graphmodels.NewConversationMember()
roles := []String {
	"owner",

}
conversationMember1.SetRoles(roles)
additionalData := map[string]interface{}{
	"@odata.type" : "#microsoft.graph.aadUserConversationMember", 
	"user@odata.bind" : "https://graph.microsoft.com/beta/users('82af01c5-f7cc-4a2e-a728-3a5df21afd9d')", 
}
conversationMember1.SetAdditionalData(additionalData)

members := []graphmodels.ConversationMemberable {
	conversationMember,
	conversationMember1,

}
requestBody.SetMembers(members)

result, err := graphClient.Chats().Post(requestBody)


```