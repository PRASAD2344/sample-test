1. Create a ASP.net controller based web API. Take a look at https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-7.0&tabs=visual-studio
   1. We don't need to have DBContext or any DB interactions for this sample.
   2. We don't need MVC.
   3. Take a look at https://learn.microsoft.com/en-us/dotnet/architecture/modern-web-apps-azure/common-web-application-architectures for project structure.
2. Expose GET endpoint and when called should return a UUID.
   1. We should get UUID's by calling API. Please look at https://www.uuidgenerator.net/api for API to retrieve UUID's.
   2. Idea is that instead of calling external API each time when we make REST API call to our code. We should store some UUID's in memory, and send it.
   3. Whenever a UUID is returned/used, we should not send it again.
   4. Handle scenario where we shouldn't return the same UUID when our API is called at the same time by different browsers.
   5. When UUIDs in memory were below threshold or not available at all(when application startup), we should make external API call to retrieve UUIDs.
   6. Handle scenario where we have no usable UUIDs in memory, and multiple uses request UUID. Only one should make API call to retrieve UUIDs, and the others should wait until some UUIDs were present in memory. And then return UUID from memory.
3. It's not mandatory but try to add test cases. But not mandatory.
   1. https://learn.microsoft.com/en-us/shows/visual-studio-toolbox/unit-testing-moq-framework
   2. https://methodpoet.com/unit-testing-with-moq/
4. Try to work on weekdays(5 AM - 10 AM), so that you will know if you can handle both.

Tools To Use:
1. Visual Studio
2. Postman
