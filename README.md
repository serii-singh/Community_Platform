## Community Platform

## Project Overview

**Community Platform** is a web-based application designed to help students, tutors, and admins connect, collaborate, and manage learning activities. The platform offers role-based dashboards, event management, resources, and interactive chat rooms. It supports user authentication via Google OAuth and mock login functionality, allowing users to interact and manage their profiles according to their roles.

## Additional Information

This is the structure and few key functionality of the projects and there are potential improvements ad bug fixation need with refactoring code nad making a diffent data page or service file for proper Api handling .


## Key Features:

-  **User Authentication**: Google OAuth login and role-based access.       
-  **Dashboards**: Role-specific dashboards for students, tutors, and admins.
-  **Event Management**: View and register for events.
-  **Teaching Resources**: Browse, bookmark, and review various teaching materials.
-  **Chat Room**: Real-time chat functionality with threaded messages.
-  **Calendar**: View upcoming events and important dates.
-  **Admin Capabilities**: Admins can manage users and content.
-  **Insights** : Admin can view the insights of the student and teacher , interactions and their news and messgaes and get 
   the data for bteer buisness prespective (implemented in mvp-2)
-  **Classroom** : For tutors and Students to schedule or view classes/videos/tutorials
-  **Messgaes** : For communication between the users .
-  **PROFILE** : Created when the useris registered and given an id . On login the user will et access to profile and Email    name can predefined and id can be used as unique key . Photos and bio are editable fields and secondary email is a 
   future plan .






# Getting Started with Create React App
This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Setup Instructions
1. Clone the repository:
Use git commands to clone repo  git clone https://github.com/serii-singh/Community_Platform.git (THE LINK IN THE HTTPS)
2. Install the dependencies:
   Commnad :-  npm i
3. Run the project
   Commnad :-  npn start
Also , Create a .env file in the root directory and add your Google OAuth client ID (optional for Google login):
REACT_APP_GOOGLE_CLIENT_ID=your-google-client-id

 Available Scripts
In the project directory, you can run:
`npm start`
Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.
The page will reload when you make changes.\
You may also see any lint errors in the console.

`npm test`
Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

`npm run build`
Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.
The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.
`npm run eject`
**Note: this is a one-way operation. Once you `eject`, you can't go back!**
If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.
Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.
You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

## API Documentation

The project uses mock functions for authentication, which interact with localStorage to store and retrieve user data.

mockLogin(email, password, requiredRole): Authenticates users based on their email, password, and role.
Returns user data if successful, or an error message if authentication fails.

getUserFromToken(): Retrieves user data from localStorage.

logout(): Logs the user out by clearing data from localStorage.

const { user, error } = mockLogin('*******.com', '***password', 'role');
if (error) {
  console.error(error);
} else {
  console.log(user);
}

## Components:
-**Auth Components**: Handle user registration, login, and profile management.
-**Dashboard Components**: Manage dashboards for students, tutors, and admins.
-**Pages**: Represent different sections of the platform, such as the community page, events, chat rooms, and resources.
-**Layout Components**: Include common elements like navigation bars and sidebars.
-**Utils**: Includes helper functions for authentication.

## Tech Stack

- **Frontend:**
  - **React**: For building the user interface.
  - **Tailwind CSS**: For utility-first styling and responsive design.
  - **React Router**: For client-side routing and navigation.
  - **React Hook Form**: For form handling and validation.
  - **@react-oauth/google**: For Google OAuth integration.

- **Backend (for future development)**:
  - Mock data and `localStorage` are currently used. The real backend will be implemented later.
    
 - **Databases**
 - Mock data is used , we can use Sql or NoSql according to the requirements.
