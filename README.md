# airbnb-clone-project

## Project Overview

This project is designed to help you improve your skills in modern software development.  
By working on this project, you will learn how to:

- Work effectively with a team using **GitHub**.
- Understand **backend architecture** and **database design** better.
- Add **security features** when building APIs.
- Create and manage **CI/CD pipelines** for faster and smoother deployments.
- Plan and **document software projects** in a professional way.

This will enable us learn and understand software development lifecycles practices, security,
CI/CD and database design ath the end of the program.

## Tech Stack
we will be using stack like **Django**, **MySQL** and **GraphQL**, **PostgreSQL**, **Celery**, **Redis**, **Docker**, **CI/CD Pipelines**


## Team Roles

### Product Owner / Manager  
Defines the project vision, sets priorities, and ensures the final product meets user needs.

### Business Analyst  
Bridges business goals and technical requirements; translates needs into clear user stories.

### Software Architect  
Designs the system structure, selects technologies, and ensures technical consistency.

### Backend Developer  
Builds APIs, manages server logic, ensures security, and integrates with databases.

### Database Administrator (DBA)  
Designs, manages, and secures the database; ensures performance and reliability.

### QA / Test Engineer  
Tests features, finds bugs, and ensures the system meets quality standards.

### DevOps Engineer  
Automates deployment, manages CI/CD pipelines, and maintains system uptime and scalability.

## Technology Stack

### Django: 
A high-level Python web framework used for building the RESTful API.

### Django REST Framework: 
Provides tools for creating and managing RESTful APIs.

### PostgreSQL: 
A powerful relational database used for data storage.

### GraphQL: 
Allows for flexible and efficient querying of data.

### Celery: 
For handling asynchronous tasks such as sending notifications or processing payments.

### Redis: 
Used for caching and session management.

### Docker: 
Containerization tool for consistent development and deployment environments.

### CI/CD Pipelines: 
Automated pipelines for testing and deploying code changes.

## Database Design

### Objective  
Understand how the database will be structured to support the Airbnb Clone project.

### Key Entities and Relationships

#### 1. Users  
- **Fields:**  
  - `id`: Unique identifier for each user  
  - `username`: The user’s login name  
  - `email`: User’s email address  
  - `password`: Hashed password for authentication  
  - `role`: Defines if the user is a host or guest  

**Relationship:**  
A user can create multiple properties and make multiple bookings.

#### 2. Properties  
- **Fields:**  
  - `id`: Unique property identifier  
  - `title`: Property name or short description  
  - `description`: Detailed information about the property  
  - `price_per_night`: Cost per night  
  - `owner_id`: References the user who owns the property  

**Relationship:**  
Each property belongs to one user (host) and can have multiple bookings and reviews.

#### 3. Bookings  
- **Fields:**  
  - `id`: Booking ID  
  - `user_id`: User who made the booking  
  - `property_id`: Property being booked  
  - `check_in_date`: Start date of the stay  
  - `check_out_date`: End date of the stay  

**Relationship:**  
A booking belongs to one user and one property.

#### 4. Reviews  
- **Fields:**  
  - `id`: Review ID  
  - `user_id`: User who wrote the review  
  - `property_id`: Property being reviewed  
  - `rating`: Numeric score given by the user  
  - `comment`: Feedback left by the user  

**Relationship:**  
Each review is written by one user for one property.

#### 5. Payments  
- **Fields:**  
  - `id`: Payment transaction ID  
  - `booking_id`: References the associated booking  
  - `amount`: Payment amount  
  - `status`: Payment status (e.g., success, failed, pending)  
  - `payment_date`: When the transaction occurred  

**Relationship:**  
Each payment is linked to one booking.

## Feature Breakdown

### User Management  
Handles user registration, authentication, and profile management.  
This ensures secure access for guests and hosts while maintaining individual profiles and roles.

### Property Management  
Allows hosts to create, update, and manage property listings.  
This feature helps users browse available accommodations with accurate information and pricing.

### Booking System  
Enables users to reserve properties for specific dates and manage booking details.  
It ensures accurate tracking of property availability and user reservations.

### Payment Processing  
Handles secure payment transactions for bookings.  
It ensures safe financial exchanges and proper record-keeping for completed stays.

### Review System  
Allows users to leave ratings and feedback on properties.  
This feature builds trust and improves transparency between hosts and guests.

### Data Optimization  
Implements caching and indexing for faster data access.  
It improves app performance and provides a smoother experience for all users.

## API Security

### Objective  
Ensure secure interaction between users and the backend services.

### Key Security Measures
- **Authentication:**  
  Only registered users can access certain endpoints using tokens (e.g., JWT).  
  This prevents unauthorized access to user or booking data.

- **Authorization:**  
  Controls what each user role (guest or host) can do.  
  For example, a host can edit their property, but a guest cannot.

- **Rate Limiting:**  
  Limits the number of API requests within a timeframe.  
  This protects against abuse such as brute-force attacks.

- **Data Encryption:**  
  All sensitive data (e.g., passwords, payment info) is encrypted.  
  This ensures user and transaction data remain private.

**Why It’s Crucial:**  
Security protects user information, prevents financial fraud, and maintains user trust in the platform.
