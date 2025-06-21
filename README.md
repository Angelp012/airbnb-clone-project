# Airbnb-clone-project
The Airbnb Clone Project is a backend simulation of a real-world booking platform. It is built to deliver a reliable and scalable system that handles user interactions, property listings, reservations, and payment processing. The project focuses on developing secure and efficient backend systems that replicate Airbnb’s core features using modern tools and best practices.

# Project Goals
* User Management: Implement a secure system for user registration, authentication, and profile management.
* Property Management: Develop features for property listing creation, updates, and retrieval.
* Booking System: Create a booking mechanism for users to reserve properties and manage booking details.
* Payment Processing: Integrate a payment system to handle transactions and record payment details.
* Review System: Allow users to leave reviews and ratings for properties.
* Data Optimization: Ensure efficient data retrieval and storage through database optimizations.

# Technology Stack
* Django: Python-based web framework used to build the backend logic and RESTful APIs.
* Django REST Framework: A toolkit built on top of Django that makes it easier to create and manage APIs.
* PostgreSQL: open-source relational database used to store and manage application data like users,properties and bookings.
* GraphQL: Allows for flexible and efficient querying of data.
* Celery: A tool that runs jobs in the background such as sending notifications or processing payments.
* Redis: Used for caching and session management.
* Docker: Guarantees standardized development, testing, and deployment environments.
* CI/CD Pipelines: Automated pipelines for testing and deploying code changes.

# Team Roles
* Backend Developer: Builds and maintains the server-side logic, APIs, and core features like authentication, bookings, payments, and property listings.
* Database Administrator: Designs and manages the database structure, ensuring relationships between users, properties, bookings, and payments are well optimized.
* DevOps Engineer: Handles deployment, monitoring, and scaling of the backend services.
* QA Engineer: Ensures the backend functionalities are thoroughly tested and meet quality standards.
* Project Manager: Coordinates task distribution, sets milestones, tracks progress, and ensures the project stays on schedule.

# Database Design Overview
1. User

Fields: id, name, email, password, role, date_joined

A user can book properties or list their own properties as a host.

2. Property

Fields: id, title, description, location, price, host_id

A property belongs to one host and can have many bookings and reviews.

3. Booking

Fields: id, user_id, property_id, check_in, check_out, status

A booking connects a user to a property and stores reservation details.

4. Review

Fields: id, user_id, property_id, rating, comment, created_at

A review is written by a user about a property they booked.

5. Payment

Fields: id, booking_id, amount, status, payment_date

A payment is linked to a booking and tracks the transaction details.

# Feature Breakdown
User Management: Handles user registration, login, profile updates, and role-based access (e.g., guest or host).

Property Management: Hosts can list, edit, or remove properties. Each listing includes detailed descriptions and availability.

Booking System: Users can book available properties by selecting dates and confirming availability.

Payment Integration: Secure handling of payments for confirmed bookings, with status updates and history.

Review System: After a stay, users can rate and review properties to enhance community trust.

Admin Dashboard: Enables moderation of users, listings, and reported reviews.

# API Security
* Authentication:  Makes sure only logged-in users can access protected parts of the app

* Authorization: Users can only modify their own data (e.g., only a host can edit their listings).

* Rate Limiting: Prevents abuse of endpoints (especially login or search) by limiting request frequency.

* Input Validation & Sanitization: Protects the app from SQL injection and XSS attacks.

* Secure Payments: Sensitive data like payment info is encrypted and handled via secure third-party integrations.

# CI/CD Pipeline
CI/CD refers to Continuous Integration and Continuous Deployment. It streamlines the automation of testing, building, and deploying the application every time new code is introduced.This makes development faster, reduces manual errors, and keeps the app running smoothly.

Tools used include:
* GitHub Actions: Automatically runs tests and deploys updates when changes are pushed to the repository.

* Docker: Packages the app with everything it needs so it can run the same way on any server.

