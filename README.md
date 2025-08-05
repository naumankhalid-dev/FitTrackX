# Fit-Track App

**Fit-Track** is a comprehensive Android fitness tracking application built using **Java**, **XML**, and **SQLite**. It empowers users to create personalized workout routines, set and track fitness goals, log daily workouts, and visualize their progress through interactive charts. The app emphasizes clean architecture, efficient local data management, and engaging data visualization powered by MPAndroidChart.

---

## Table of Contents

- [Project Overview](#project-overview)  
- [Features & Functionalities](#features--functionalities)  
- [Database Design & DBHelper Usage](#database-design--dbhelper-usage)  
- [Skills Demonstrated](#skills-demonstrated)  
- [Technology Stack](#technology-stack)  
- [Future Enhancements](#future-enhancements)  
- [Contact](#contact)

---

## Project Overview

Fit-Track helps fitness enthusiasts maintain consistent workout habits by allowing them to register securely, build and manage workout routines, set measurable fitness goals, log daily exercise activities, and analyze progress visually. All data is stored locally using SQLite for offline access and quick retrieval, while the MPAndroidChart library provides a professional and interactive way to view fitness trends.

---

## Features & Functionalities

- **User Registration and Authentication**  
  Secure account creation and login with locally stored credentials via SQLite, ensuring quick and private authentication.

- **Workout Routine Management**  
  Create, update, view, and delete personalized workout routines with detailed exercises, sets, repetitions, and schedules.

- **Workout Logging and History**  
  Log daily workouts specifying type, duration, calories burned, and notes. Review detailed workout history filtered by date or routine.

- **Goal Setting and Tracking**  
  Define multiple fitness goals such as workout frequency, calorie targets, or duration goals. Monitor progress visually and numerically.

- **Progress Visualization**  
  Utilize **pie charts**, **bar graphs**, and **line charts** to display exercise distribution, daily activity, and progress trends using the MPAndroidChart library.

- **Integrated Workout Timer**  
  Track workout session durations in real-time to improve time management and data accuracy.

- **Offline-First Design**  
  All user data including workouts, routines, and goals are managed locally ensuring app functionality without internet connectivity.

---

## Database Design & DBHelper Usage

The app’s database is managed through a custom `DBHelper` class, extending `SQLiteOpenHelper`, responsible for all data-related operations:

### Key Tables & Relationships

| Table      | Description                            | Key Fields                         |
|------------|------------------------------------|----------------------------------|
| **Users**  | Stores user credentials and profile | `user_id (PK)`, `username`, `password`, `email` |
| **Routines** | User-specific workout plans         | `routine_id (PK)`, `user_id (FK)`, `name`, `description` |
| **Workouts** | Logged exercises and details        | `workout_id (PK)`, `user_id (FK)`, `routine_id (FK)`, `date`, `duration`, `calories` |
| **Goals**   | Fitness targets                     | `goal_id (PK)`, `user_id (FK)`, `goal_type`, `target_value`, `current_value`, `deadline` |

### DBHelper Responsibilities

- **Database Creation and Upgrades:**  
  Creates all necessary tables with foreign keys to maintain referential integrity. Manages smooth schema upgrades.

- **CRUD Operations:**  
  Implements methods to add, retrieve, update, and delete users, routines, workouts, and goals, ensuring secure and efficient data handling.

- **User Authentication:**  
  Validates user credentials and maintains session information.

- **Efficient Data Queries:**  
  Supports complex queries for workout history, goal progress, and analytics to feed the charting components.

- **Transaction Management:**  
  Uses transactions where needed to preserve data consistency during multiple related database operations.

- **Data Integrity and Security:**  
  Enforces constraints and handles exceptions to maintain robust database health.

---

## Skills Demonstrated

- **Android Development:**  
  Building a full-featured Android app using Java and XML with best practices.

- **Database Design & Management:**  
  Designing normalized SQLite database schemas with relational integrity and efficient CRUD operations.

- **UI/UX & Data Visualization:**  
  Creating user-friendly layouts and integrating MPAndroidChart for rich visual feedback.

- **Software Architecture:**  
  Applying modular design and separation of concerns for scalable and maintainable code.

- **Offline-First Mobile Application Design:**  
  Ensuring all features work seamlessly without internet connectivity.

---

## Technology Stack

| Technology      | Role                             |
|-----------------|---------------------------------|
| Java            | Application logic and backend   |
| XML             | UI layouts and design           |
| SQLite          | Local persistent storage        |
| MPAndroidChart  | Charts and data visualization   |
| Android Studio  | Development environment         |

---

## Future Enhancements

- Cloud synchronization with Firebase for data backup and multi-device support.  
- Push notifications to remind users about workouts and goals.  
- Dark mode for improved usability in low-light environments.  
- AI-driven workout suggestions based on user progress.  
- Social sharing features for motivation and community engagement.


---

## Contact

**Nauman Khalid**  
- GitHub: [https://github.com/naumankhalid-dev](https://github.com/naumankhalid-dev)  
- LinkedIn: [https://www.linkedin.com/in/nauman-khalid-58a2692a0](https://www.linkedin.com/in/nauman-khalid-58a2692a0)

---

*Empowering your fitness journey through clean code, reliable data management, and engaging design.*
