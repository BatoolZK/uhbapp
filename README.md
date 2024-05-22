# UHBAPP Application

## Overview

The University Hub Application is designed to facilitate communication and manage various academic functionalities for students, teachers, and administrators within the University of Hafr Al Batin. The application provides features for student enrollment, course management, chatting, and excuse submissions, among others.

## Features

- **Student Enrollment**: Students can enroll in courses based on their level and access permissions.
- **Course Management**: Teachers can view assigned courses and manage excuses submitted by students.
- **Chat System**: A chat system for communication between students and teachers.
- **Profile Management**: Users can manage their profile information, including profile pictures.
- **Search Functionality**: Administrators can search for students and view their details and enrolled courses.
- **Excuse Submission**: Students can submit excuses for absences with image attachments, which can be reviewed by teachers.

## Technologies Used

- **Flutter**: For the mobile application framework.
- **Firebase**: For authentication, Firestore for database, and Firebase Storage for storing images.
- **Dart**: The programming language used with Flutter.

## Installation

1. **Clone the repository**
   ```bash
   git clone https://.git
   cd university-app

2. **Install dependencies**
   ```bash
   flutter pub get

3. **Setup Firebase**
   ```bash
   Create a Firebase project in the Firebase Console.
   Add your Android app to the Firebase project.
   Download the google-services.json file for Android and place it in the android/app directory.
   Enable Firestore, Authentication, and Storage in your Firebase project.
4. **Run the application**
   ```bash
   flutter run

# Usage
## Profile Management
Users can update their profile information including their profile picture.

## Enrollment
Students can enroll in courses based on their access level. The enrollment process ensures that courses are not duplicated and are distributed evenly throughout the week.

## Course Management
Teachers can view their assigned courses, manage students' excuses for absences, and communicate with students through the chat system.

## Chat System
The chat system allows for easy communication between students and teachers, with the ability to filter chats and show the most recent messages.

## Excuse Submission
Students can submit excuses for absences with an image attachment, which teachers can approve or reject.

# Firebase Collections Structure
## Users
Collection Name: users
Fields:
firstName: String
lastName: String
email: String
type: String (student, teacher, or admin)
studentID: String (for students)
## Courses
Collection Name: courses
Fields:
code: String
name: String
day: String
hour: Number
duration: Number
instructor: String (email of the instructor)
level: Number
description: String (optional)
## Student Courses
Collection Name: student_courses
Fields:
userId: String (user ID of the student)
courseCode: String
courseName: String
level: Number
grade: String (nullable)
## Excuses
Collection Name: excuses
Fields:
userId: String (user ID of the student)
courseCode: String
excuse: String
date: Timestamp
approved: Boolean (nullable)
imageUrl: String (URL of the uploaded image)


