---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


graphClient.Education().ClassesById("educationClass-id").AssignmentsById("educationAssignment-id").CategoriesById("educationCategory-id").Ref().Delete(context.Background(), nil)


```