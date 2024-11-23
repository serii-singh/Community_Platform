## Community Platform

## Project Overview

**Community Platform** is a web-based application designed to help students, tutors, and admins connect, collaborate, and manage learning activities. The platform offers role-based dashboards, event management, resources, and interactive chat rooms. It supports user authentication via Google OAuth and mock login functionality, allowing users to interact and manage their profiles according to their roles.

## Additional Information

This is the structure and few key functionality of the projects and there are potential improvements ad bug fixation need with refactoring code nad making a diffent data page or service file for proper Api handling .


## Key Features:

-  **User Authentication**: Google OAuth login and role-based access.
-  **Registration and Login** : Role based resitration and login access to user on the basis of which dashboard apperas . 
      In addition , the tutaor registartion will follow a different journey after normal registatrion is future plans       
-  **Dashboards**: Role-specific dashboards for students, tutors, and admins.Also , different roles will have different 
    access to pages like only admin will view everything for now and tutors and students will not be ble to view features l 
    like Insights etc and will be redirecte to 404 error/login for now. In further developments, user will not view the 
    features which is unaccesible .
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
   **Responsive and reusable components**






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

`npm run build`
Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.
The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!


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
  - Mock data and localStorage are currently used. The real backend will be implemented later.
    
 - **Databases**
 - Mock data is used , we can use Sql or NoSql according to the requirements.


## Future improvements

- Expand user roles with specific permissions.
- UI corrects across the web
- Refactoring of code components to make it work on functions and make more dynamic using same components and functions 
  from servivce files .
-  Implement SEO , lazy loading (integrate images as there are no images currently )
-  More powerful implementation of protected routes and bug fixes like back button navigation fixes .
-  Make role specific dynamic key functioanlity
-  Calendar Enhancements: Add more interactive features, such as event reminders and scheduling.
-  Profile Enhacements


##Project architecture 

The frontend of the Community Platform is built using React, which is responsible for rendering the user interface and managing user interactions. The React app follows a component-based architecture, with each component serving a distinct part of the application. It interacts with the backend via API calls (once implemented) or mock data stored in localStorage.

Key Components:
- Auth Components: RegistrationForm, LoginForm, Profile
- Handles user authentication and profile management.
- Integrates Google OAuth for authentication.
-  Dashboard Components: StudentDashboard, TutorDashboard, AdminDashboard
- Displays role-specific content based on user roles (student, tutor, admin).
- Pages: CommunityPage, Events, TeachingResources, Messages, Insights, ChatRoom, Classroom, Calendar
- Displays various sections of the platform, like community posts, events, and chat rooms.
- Layout Components: NavBar, Sidebar, DashboardLayout
- Provides common structure and navigation throughout the app.
  
Frontend Flow:
User Registration/Login: Handled by RegistrationForm and LoginForm components using form validation and authentication.
Role-Based Content: Based on the authenticated user's role, they are redirected to their respective dashboards (StudentDashboard, TutorDashboard, AdminDashboard).
Page Content: Users can navigate through various pages like CommunityPage, ChatRoom, Events, etc., based on their role.
State Management: Utilizes React Context API to manage user authentication and role-based data.

##Flow and Security Considerations
User Authentication: The system will authenticate users with JWT (for stateless authentication) or OAuth via Google. This ensures that users can securely log in and access only the content relevant to their roles.

Role-Based Access: Each route/component will check the user's role (admin, tutor, student) and render the appropriate UI. Unauthorized access will be redirected to an error page or login page.

This structure ensures scalability, easy management, and the ability to add more features in the future as the platform grows.
