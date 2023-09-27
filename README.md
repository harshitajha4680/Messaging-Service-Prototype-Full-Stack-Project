# Task: Build a Messaging Service Prototype


## Requirements - 
1. Messaging Service Features: Your prototype should include the following core features:
User registration and authentication.
2. Sending and receiving text messages between users.
3. Group chat functionality.
4. Real-time message updates.
5. Optional Features:  You can also include these features:
6. AI powered chatbot for user.
7. Video calling or audio calling feature.
8. Design: User interface should be clean and intuitive.
9. App type: Any web app (preferably reactjs) or mobile app can be used. Using specific practices such as Atomic 
10. Design would be a plus.
11. Backend: Develop REST APIs using best practices. Any programming language can be used (preferably python and
12. nodejs). Also choose between noSQL and SQL database.
13. Documentation: Create a system design document and also provide clear documentation on how to set up and run your prototype, including any dependencies and libraries used and also provide details about why you used them.


# Documentation:
![Plan](https://github.com/harshitajha4680/Messaging-Service-Prototype-Full-Stack-Project/blob/main/COMPLETE_PLAN.png)

# Tech Stack
![Plan](https://github.com/harshitajha4680/Messaging-Service-Prototype-Full-Stack-Project/blob/main/Node_Mongo.jpg)

## FRONTEND -
```bash
 public
│   └── index.html
└── src
    ├── App.css
    ├── App.js
    ├── Pages
    │   ├── ChatPage.js
    │   └── HomePage.js
    ├── animations
    │   └── typing.json
    ├── background.jpg
    ├── background1.png
    ├── background2.jpg
    ├── components
    │   ├── Authentication
    │   │   ├── Login.js
    │   │   └── Signup.js
    │   ├── ChatBox.js
    │   ├── ChatLoading.js
    │   ├── MyChats.js
    │   ├── ScrollableChat.js
    │   ├── SingleChat.js
    │   ├── UserAvatar
    │   │   ├── UserBadgeItem.js
    │   │   └── UserListItem.js
    │   ├── miscellaneous
    │   │   ├── GroupChatModal.js
    │   │   ├── ProfileModal.js
    │   │   ├── SideDrawer.js
    │   │   └── UpdateGroupChatModal.js
    │   └── styles.css
    ├── config
    │   └── ChatLogics.js
    ├── context
    │   └── ChatProvider.js
    ├── index.css
    ├── index.js
    └── services
        └── helper.js

```

- **`public/index.html`**: This is the main HTML file for your web application. It likely contains the basic structure of your webpage, including the title, links to CSS and JavaScript files, and the root DOM element where your React app will be rendered.

- **`src/App.css`**: This file likely contains CSS styles specific to your entire application. It is used to style your components in a consistent way.

- **`src/App.js`**: This is likely the entry point for your React application. It may define the main layout and routing of your app.

- **`src/Pages/ChatPage.js`**: This file probably represents a page in your application dedicated to chatting functionality.

- **`src/Pages/HomePage.js`**: This file probably represents the home page of your application, which may include features like user authentication or a landing page.

- **`src/animations/typing.json`**: This file likely contains animation data in JSON format, possibly for use in your application's user interface.

- **`src/background.jpg`, `src/background1.png`, `src/background2.jpg`**: These are likely background images that can be used in your application's design.

- **`src/components/Authentication/Login.js` and `src/components/Authentication/Signup.js`**: These components likely handle user authentication, providing forms and logic for user login and registration.

- **`src/components/ChatBox.js`**: This component likely represents the chat box where users can send and receive messages.

- **`src/components/ChatLoading.js`**: This component could be responsible for displaying loading indicators while fetching chat data.

- **`src/components/MyChats.js`**: This component may represent a user's list of chats or conversations.

- **`src/components/ScrollableChat.js`**: This component might handle scrolling through chat messages, possibly with infinite scrolling.

- **`src/components/SingleChat.js`**: This component might represent an individual chat or conversation with a user or group.

- **`src/components/UserAvatar/UserBadgeItem.js` and `src/components/UserAvatar/UserListItem.js`**: These components may deal with displaying user avatars or badges in various parts of the application.

- **`src/components/miscellaneous/GroupChatModal.js`, `src/components/miscellaneous/ProfileModal.js`, `src/components/miscellaneous/SideDrawer.js`, `src/components/miscellaneous/UpdateGroupChatModal.js`**: These components could be various modal dialogs or drawers used for actions like creating group chats, updating profiles, or displaying additional information.

- **`src/components/styles.css`**: This CSS file likely contains styles specific to individual components.

- **`src/config/ChatLogics.js`**: This file might contain configuration or logic related to chat functionality.

- **`src/context/ChatProvider.js`**: This file is likely the context provider for your application, managing the state and data related to chat functionality and making it accessible to various components.

- **`src/index.css`**: This is a global CSS file that can be used to define styles that apply across your entire application.

- **`src/index.js`**: This is the entry point of your React application, where the React app is typically rendered into the DOM.

- **`src/services/helper.js`**: This file may contain utility functions or helper methods used throughout your application.
- **`config/db.js`**: This file is likely responsible for configuring your database connection. It may define how your Node.js application connects to your database, sets up a connection pool, or specifies database credentials.

- **`config/generateToken.js`**: This file could be used to generate authentication tokens, such as JSON Web Tokens (JWTs), which are commonly used for securing API endpoints and user authentication.

- **`controllers/chatControllers.js`**: This file probably contains controller functions that handle various operations related to chat functionality. These controllers may include functions for creating, updating, or deleting chats.

- **`controllers/messageControllers.js`**: This file likely contains controller functions for handling messages within your application. These controllers might include functions for sending, retrieving, or deleting messages.

- **`controllers/userControllers.js`**: This file probably contains controller functions for user-related operations, such as user registration, login, profile management, and more.

- **`data/data.js`**: This file could potentially be used to store and export sample data or initial data used during development or testing.

- **`middleware/authMiddleware.js`**: This file is likely responsible for defining middleware functions that handle authentication and authorization tasks. Middleware functions can be used to protect certain routes or perform actions before or after a request is processed.

- **`middleware/errorMiddleware.js`**: This file may define middleware functions to handle errors that occur during the processing of HTTP requests. It can help centralize error handling and improve error responses to clients.

- **`models/chatModel.js`**, **`models/messageModel.js`**, **`models/userModel.js`**: These files probably define the data models for your application. They specify the structure of data objects that will be stored in the database and may include validation and schema-related logic.

- **`package-lock.json`** and **`package.json`**: These files are part of Node.js and NPM (Node Package Manager) and contain information about your project's dependencies and metadata. `package.json` also includes scripts for running your application and managing dependencies.

- **`routes/chatRoutes.js`**, **`routes/messageRoutes.js`**, **`routes/userRoutes.js`**: These files are likely used to define the routes and associated controller functions for different parts of your API. They specify how incoming HTTP requests are mapped to specific controller actions.

- **`server.js`**: This is likely the main entry point of your backend application. It typically sets up your Express.js server, defines middleware, connects to the database, and specifies the routes that your API will listen to.


## BACKEND -

```bash
├── config
│   ├── db.js
│   └── generateToken.js
├── controllers
│   ├── chatControllers.js
│   ├── messageControllers.js
│   └── userControllers.js
├── data
│   └── data.js
├── middleware
│   ├── authMiddleware.js
│   └── errorMiddleware.js
├── models
│   ├── chatModel.js
│   ├── messageModel.js
│   └── userModel.js
├── package-lock.json
├── package.json
├── routes
│   ├── chatRoutes.js
│   ├── messageRoutes.js
│   └── userRoutes.js
└── server.js

```
- **`config/db.js`**: This file is likely responsible for configuring your database connection. It may define how your Node.js application connects to your database, sets up a connection pool, or specifies database credentials.

- **`config/generateToken.js`**: This file could be used to generate authentication tokens, such as JSON Web Tokens (JWTs), which are commonly used for securing API endpoints and user authentication.

- **`controllers/chatControllers.js`**: This file probably contains controller functions that handle various operations related to chat functionality. These controllers may include functions for creating, updating, or deleting chats.

- **`controllers/messageControllers.js`**: This file likely contains controller functions for handling messages within your application. These controllers might include functions for sending, retrieving, or deleting messages.

- **`controllers/userControllers.js`**: This file probably contains controller functions for user-related operations, such as user registration, login, profile management, and more.

- **`data/data.js`**: This file could potentially be used to store and export sample data or initial data used during development or testing.

- **`middleware/authMiddleware.js`**: This file is likely responsible for defining middleware functions that handle authentication and authorization tasks. Middleware functions can be used to protect certain routes or perform actions before or after a request is processed.

- **`middleware/errorMiddleware.js`**: This file may define middleware functions to handle errors that occur during the processing of HTTP requests. It can help centralize error handling and improve error responses to clients.

- **`models/chatModel.js`**, **`models/messageModel.js`**, **`models/userModel.js`**: These files probably define the data models for your application. They specify the structure of data objects that will be stored in the database and may include validation and schema-related logic.

- **`package-lock.json`** and **`package.json`**: These files are part of Node.js and NPM (Node Package Manager) and contain information about your project's dependencies and metadata. `package.json` also includes scripts for running your application and managing dependencies.

- **`routes/chatRoutes.js`**, **`routes/messageRoutes.js`**, **`routes/userRoutes.js`**: These files are likely used to define the routes and associated controller functions for different parts of your API. They specify how incoming HTTP requests are mapped to specific controller actions.

- **`server.js`**: This is likely the main entry point of your backend application. It typically sets up your Express.js server, defines middleware, connects to the database, and specifies the routes that your API will listen to.
