---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestFilter := "isof or isof"

requestParameters := &graphconfig.DirectoryObjectsDelta()RequestBuilderGetQueryParameters{
	Filter: &requestFilter,
	Select: [] string {"microsoft.graph.user/surname","microsoft.graph.group/displayName"},
}
configuration := &graphconfig.DirectoryObjectsDelta()RequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.DirectoryObjects().Delta().Get(context.Background(), configuration)


```