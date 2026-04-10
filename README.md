# Campsite Reservation System

## Project Overview
The **Campsite Reservation System** allows users to book and review campsites across some locations in Malaysia. There are multiple accommodation types including tents, cabins, RV sites, and glamping options.

The goal is to demonstrate understanding of:
- Inheritance
- Polymorphism
- Interfaces
- File handling / Database integration
- Exception handling

The final deliverable is a console‑based application, complete with requirements specification

## System Requirements Specification(SRS)
### Functional Requirements (At Lease 8 core functionalities)
The functionalities included: 
1. User Registration
2. User Login
3. Searching for Available Campsites Spots by Location or Types
4. Making Reservation
5. Cancellation of Reservation
6. Payment Processing
7. Reviews/Feedbacks
8. Admin Registration
9. Campsites Management
10. View All Reservation
11. View Feedbacks
12. Report Management

| Functionality | Description | Precondition |
|-----------|-----------------|------------------|
| **User Registration** | New user or administrator can sign up by UserName  | - Invalid for existed user <br /> - Invalid for wrong format of password <br /> - Password and Confirm Password must be matched |
| **User Login** | New user or administrator can log in by using specific User ID or UserName | - User must be registered in system <br /> - Valid UserID/UserName <br /> - Valid Password |
| **Viewing Details** | View campsites, cabins, glamping spots, price or capacity | User must be logged in |
| **Searching for Available Campsites Spots by Location or Types** |  Users search based on filter criteria | - User must be logged in <br /> - Campsites data must available in system  |
| **Making Reservation** | Reserves a campsite with date and guest validation | - User must be logged in <br /> - Campsite must be available for selected dates <br /> - Must not exceed the campsite capacity |
| **Cancellation of Reservation** | Cancel existing reservation from both memory list and text file | - User must be logged in <br /> - Reservation must exist |
| **Payment Processing** | Handle payment for reservations via multiple payment methods | - User must be logged in <br /> - Must have unpaid reservations |
| **Reviews / Feedbacks** | Submit reviews, comments and ratings for certain campsites | User must be logged in |
| **Admin Registration** | Allows an authenticated administrator to register a new admin account with a new username and password | An existing admin must be logged in to access this functionality. The chosen username must not already exist, and the password must be at least 8 characters long, containing uppercase letters, lowercase letters, and numbers |
| **Manage Campsites** | Allows admin to add, modify, or delete campsites | The user must be logged in as an admin |
| **View all Reservation** | Allows admin to view all reservation made by users | - Admin must be logged in <br /> - Reservation data must exist |
| **View feedback** | Allows admin to access and review feedback written by users | - Admin must be logged in <br /> - Feedback record must exist |
| **Manage report** | Allows admin to review, add, modify, delete reports | - Admin must be logged in <br /> - Report must exist |

## Project Structure
```bash
CampingSystem/
│
├── RunCampsiteSystem.bat  # Windows launcher
├── CampingSystem.jar      # Main Java executable
│
├── Admin Package Files
│   ├── Admin.java
│   ├── AdminManager.java
│   ├── AdminPortal.java
│   ├── AdminService.java
│   ├── Campsite.java
│   ├── CampsiteManager.java
│   ├── CampsiteService.java
│   ├── Filterable.java
│   ├── Report.java
│   ├── ReportData.java
│   ├── ReportService.java
│   ├── ReservationViewer.java
│   ├── Review.java
│   └── ViewReview.java
│
├── User Package Files
│   ├── AuthService.java
│   ├── FileService.java
│   ├── MainMenu.java
│   ├── Menu.java
│   ├── PaymentData.java
│   ├── PaymentMenu.java
│   ├── PaymentService.java
│   ├── ReservationData.java
│   ├── ReservationMenu.java
│   ├── ReservationService.java
│   ├── ReviewMenu.java
│   ├── ReviewService.java
│   ├── User.java
│   └── UserPortal.java
│
├── user_Info.txt
├── regions.txt
├── campsite_Types.txt
├── campsites_Info.txt
├── reserves.txt
├── payments.txt
├── review.txt
└── report.txt
```
