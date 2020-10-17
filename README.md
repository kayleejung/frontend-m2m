# Frontend and Mobile
If you have not already, please read the [docs](https://github.com/UBC-BEST/m2m-docs) first then come back here! 
- [General App Architecture](https://developer.android.com/jetpack/guide)
- [Setting up Unity](https://medium.com/@razvan_57516/how-to-embed-unity-3d-in-a-native-android-app-5d030673bbf4)
- [PLEASE READ: Getting started with Kotlin MMP](https://kotlinlang.org/docs/mobile/create-first-app.html)

## User Research/Design Process 
[Wireframes and Prototypes](https://www.justinmind.com/blog/whats-the-difference-between-wireframes-and-prototypes/#:~:text=To%20break%20it%20down%2C%20website,more%20visual%20detail%20and%20interaction.&text=Read%20on%20for%20more%20on,web%20or%20mobile%20design%20process.)
- In the coming weeks, our designer will produce low-fi skethces, wireframe and prototype. We will iterate on their original designs.

## Frontend Development
We will be following the [MVC pattern](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller), or Model-view-Controller pattern. 
![mvc](/photos/mvc.png "mvc")

### Why use Model-view-Controller?
- This design pattern divides business logic into 3 interconnected elements. 
- This limits the user from seeing the internal structure of the application and it also seperates components from each other in that when we make a change in one part of the code we don't have to go chasing for errors in other portions. 
- When executed correctly, if we were is make a change in the model, we would not have to make changes in the view or the controller. 
- This way our code is not prone to dependencies and is able to adopt to changes quickly and robustly. 

## Model
The model represents the data of the application and is independent of the user interface. It has **DIRECT** accesses to the data. Stuff that happens in the model includes acssessing data from the database or changing the data in some way. So far, our model has these classes: 

| Class | Attributes | Methods Associated |
|---|---|---|
| User | - personal data such as name |`getData(),updateData()`| 
|   |   |   |  
|   |   |   |  

### User
The user class represents a User that has attributes:
- personal data such as name  
- uid/token 
- Register, Login, Retrieve/Send user data to the cloud
### Game
- Flappy Bird: Record User scores and send to the cloud
### Sensor 
- Send/receive sensor data to the cloud
### Networking
- Sync local data with remote server

## View 
This can simply be thought of as what the user sees, or the user interface. All this component does is display information. There should be almost no logic in dealing with data processing or manipulation 

## Controller 
When the user interacts with the user interface, the controller either directs these actions to the view or the model. For instance, if the user is playing a game and clicks on a button, the user data will be sent to the model and the change in the appearance of the button will be sent to the view. 

## Code Styles 
- Add the [Dokka](https://github.com/Kotlin/dokka) plugin before you start writing docstrings. 
- If you want to read the official documentation, click [here](https://kotlinlang.org/docs/reference/kotlin-doc.html).
### Class
- for each class, make a new file 
- at the top of the file, make a comment about what the class represents

### Method 

## Start coding! 
When coding please follow style guides and make meaningful comments. 
