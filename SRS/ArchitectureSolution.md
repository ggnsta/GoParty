# Architechture solution research

### 1. Application type
  GoParty is a `Mobile Application`. This type was chosen becuase nowadays smartphones are getting all over the place and are being integrated in our lives deeply. This type provides availability and simplicity of usage.
The application itself is supposed to:
* Have a minimalistic user-friendly interface
* Use internet resources wisely and be able to sustain its work with flaky internet connection
* Optimize the amount of used storage and processing resources

### 2. Deploying strategy

  GoParty application has a `distributed` `client-server` deployment model. The back end of the application is storing and processing data on one server, so that the database is not separated from the represenation model. This solution makes the architechture less flexible but provides greater performance and  less code complexity.

### 3. Technologies description

| Objective | Technology (and/or Language) | 
|:---|:---|
|Mobile client|Kotlin|
|Server application|.NET Framework|
|Web server|Internet Information Services (IIS)|
|Database configuration|SQL Server Managment Studio|
|Database server|MS SQL Server|
|IDE|MS Visual Studio, Android Studio|

1) For mobile client development Kotlin was chosen as a primary language, because of its high popularity, good support from Google and its performance (in context of Android-based systems)
2) .NET helps to develop high quality applications faster. Modern language constructs like generics, Language Integrated Query (LINQ), and asynchronous programming make developers productive. The ASP.NET Web API is an extensible framework for building HTTP based services that can be accessed in different applications on different platforms such as web, windows, mobile etc.
3)  With the Entity Framework, developers can work at a higher level of abstraction when they deal with data, and can create and maintain data-oriented applications with less code compared with traditional applications.

### 4. Quality markers
Here are listed all the important  quality markers

| Category |  Quality marker| 
|:---|:---|
|Desing quality|Conceptual integrity|
|Runtime qualuty|Availabilty|
||Performance|
||Reliablity|
||Security|
|User interface quality|Convinience and usage simplicity|

### 5. Ways to implement end-to-end functionality
* Authentication is based on the OAuth2 protocol that contains encrypted user information.
* Network communication between client and server occurs via Http requests.
* The configuration of the application is stored on the server as an xml file.
* Exception management with exception handlers which are included in the framework pipeline.
### 6. Application structure
![structure](https://github.com/NasterVill/GoParty/blob/master/Resources/Diagrams/Structure.PNG)
### 7. Arcitecture 'As Is' and 'To be'
![arcitecture](https://github.com/NasterVill/GoParty/blob/master/Resources/Diagrams/Architecture(Back%20end).PNG)

  The stair architecture (Stairway pattern) is a variation of the classical three-layer architecture with the Dependency Inversion Principle. As a result of this pattern, the system becomes more resistant to change. If you change the implementation of each level, you do not have to change the rest, if the interaction between them remains unchanged. This flexibility is achieved both by providing strong cohesion (high cohension) and weak coupling (low coupling) components of the application.
## Comparison:
  In general architectural idea was successfully implemented. But there are some issues inside of concrete layers. All of this differences are trivial and temporarily that's why it's not shown on another diagram. 
  
## Ways of improvement:
  1. Move mappers to separated interface 
  2. Improve exception handling mechanism
  3. Utilize DependencyResolver component due to using NinjectModule implementation for each binding context.
  
  
