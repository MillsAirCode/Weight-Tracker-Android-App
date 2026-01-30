# Weight Tracker Android App

This is a simple Android application built with Java in Android Studio that allows users to register, log in, track their weight over time, and visualize their progress in a chart. The app uses SQLite for data storage and includes basic permission handling.

## Features

- **User Authentication**: Register and log in with a username and password (minimum 6 characters).
- **Weight Tracking**: Add, update, delete, and view weight entries with dates.
- **Data Persistence**: Stores user data and weight entries in an SQLite database.
- **Data Display**: Shows all weight entries in a list view.
- **Chart Visualization**: Displays weight data in a WebView using a local HTML chart (loaded from assets).
- **Permission Handling**: Requests SMS permission (demonstrates runtime permissions, though SMS functionality is placeholder).

## Key Components

- **`DatabaseHelper.java`**: Manages SQLite database creation and operations (users and weight entries tables).
- **`LoginActivity.java`**: Handles user login and registration with SharedPreferences for session management.
- **`MainActivity.java`**: Main screen with navigation to login, data display, chart, and permission request activities.
- **`DataDisplayActivity.java`**: Allows users to input and view weight entries.
- **`ChartActivity.java`**: Renders a chart using a WebView and JavaScript, pulling data from the database.
- **`PermissionRequestActivity.java`**: Demonstrates requesting SMS permission (placeholder functionality).
- **`WeightEntry.java`**: Model class for weight entry data.

## Database Schema

- **Users Table**: Stores `id` (auto-increment), `username` (unique), and `password`.
- **Weight Entries Table**: Stores `id` (auto-increment), `date`, `weight`, and `user_id` (foreign key to Users).

## Build Configuration

The app uses a Gradle build configuration written in Kotlin Script (`build.gradle.kts`). Key settings include:

- **Namespace**: `com.example.androidstudiointro`
- **SDK Versions**: 
  - Compile SDK: 34
  - Minimum SDK: 28
  - Target SDK: 34
- **Version**: 1.0 (versionCode: 1)
- **Dependencies**:
  - AndroidX libraries: `appcompat`, `material`, `activity`, `constraintlayout`, `recyclerview`
  - Gson: `com.google.code.gson:gson:2.10.1`
  - Testing: `junit`, `ext.junit`, `espresso.core`
- **Java Compatibility**: Java 8
- **Build Types**: Release build with minification disabled and default ProGuard rules.

See `app/build.gradle.kts` for the full configuration.

## Usage

1. Launch the app and navigate to the login screen from the main activity.
2. Register a new account or log in with existing credentials.
3. Add weight entries with dates in the data display screen.
4. View all entries in a list or visualize them in the chart activity.
5. Optionally, test SMS permission requesting (no actual SMS sent).

## Requirements

- Android Studio
- Minimum API level 28 (Android 9.0 Pie)
- Local `chart.html` file in the `assets` folder for chart rendering

## Notes

- Passwords are stored in plain text (for simplicity; consider encryption in production).
- The chart relies on a JavaScript function (`drawChart`) in `chart.html`, which is not included here.
- SMS functionality is a placeholder and requires further implementation.


Introduction


The Weight Tracker application was created to assist individuals in monitoring their weight and advancements towards achieving their fitness objectives. The primary goal of the app is to cater to users requirement, for an user friendly tool for monitoring weight fluctuations over time thereby aiding in the management of their health and fitness journey.

Interface


The application encompasses screens and functionalities to meet user requirements and deliver a user centric interface;

Sign In Page; Users can securely log into their accounts to access personalized weight tracking information.
Weight Input Page; Enables users to enter their weight for a date allowing them to monitor their progress over time.
Visual Representation; Displays users with a representation of their weight data across timelines facilitating the tracking of trends and progress.
Profile Management; Users have the ability to modify their profile details and personalize their weight tracking settings.
The UI designs were meticulously developed with users, in focus emphasizing simplicity, clarity and ease of navigation. The incorporation of layouts, intuitive navigation paths and clear visual indicators was aimed at ensuring an user experience. Through the integration of user feedback and an iterative design approach the UI designs effectively met user expectations while enhancing usability.

Approach to Development


The application was coded using Java, within Android Studio adhering to the principles of object oriented programming and the Model View Controller (MVC) architecture. To enhance maintainability and scalability, modular and reusable code components were incorporated. Embracing integration and version control practices aided in streamlining development processes and fostering collaboration among team members.

Testing served as a step in ensuring the effectiveness and dependability of the code. Unit tests were carried out to validate code components while integration tests were executed to evaluate the system performance. A comprehensive testing approach enabled the identification and resolution of any bugs or challenges thereby guaranteeing an reliable application.

Innovation and Obstacles


A challenge encountered during development involved creating visually appealing and informative graphical representations of weight data. By utilizing charting libraries and customization features this obstacle was successfully navigated, resulting in an enlightening visualization for users.

Demonstrated Proficiency


The integration of weight tracking functionality highlighted expertise in data management, UI design and application architecture. Through leveraging functionalities within Android Studio and adhering to industry standards the application showcased an understanding of knowledge, skills and experience, in mobile app development.

## Author

Brad Mills ([@MillsAirCode](https://github.com/MillsAirCode))

