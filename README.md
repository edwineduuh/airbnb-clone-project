# airbnb-clone-project
This project is a  clone of Airbnb, designed to practice by Backend development skills

## Project Goals
- Build a clone version of Airbnb
- Practice advanced backend skills
- Learn teamwork and project management skills

## Tech stack
- Python
- Django
- Django REST Framework
- PostgreSQL
- GraphQl
- Celery
- CI/CD
- Docker
## Team Roles

### Backend Developer
The **Backend Developer** is responsible for building the server side logic and ensuring smooth communication between the frontend and the database. They will:
- Develop APIS
- Handle authentication and authorization
- Integrate third-party services
- OPtimize backend performance

### Frontend Developer
The **Frontend Developer**  focuses in creating interface (UI) of the website, ensuring a responsive and seamless user experince. They will:
- Design and implement the website's layout and design.
- Ensure it works across all devices
- Implement interactivity with Javascript

### 🛢️ Database Administrator (DBA)
- Designs and manages the database schema.
- Ensures data is stored securely and efficiently.
- Works with tools like MySQL or PostgreSQL.

### 🔍 Quality Assurance (QA) Tester
- Tests the application for bugs and errors.
- Ensures features work as expected before deployment.
- Writes and runs test cases.

### ☁️ DevOps Engineer
- Sets up the deployment and CI/CD pipeline.
- Automates development, testing, and deployment.
- Manages the hosting environment (e.g., Heroku, AWS, or Docker).

### ✍️ Technical Writer
- Writes clear documentation for users and developers.
- Updates the README, guides, and API references.


### Technology Stack
- Django: A high-level Python web framework used for building the RESTful API.
- Django REST Framework: Provides tools for creating and managing RESTful APIs.
- PostgreSQL: A powerful relational database used for data storage.
- GraphQL: Allows for flexible and efficient querying of data.
- Celery: For handling asynchronous tasks such as sending notifications or processing payments.
- Redis: Used for caching and session management.
- Docker: Containerization tool for consistent development and deployment environments.
- CI/CD Pipelines: Automated pipelines for testing and deploying code changes.
### Database Design
## Key Entities and Fields
## User
- id (Primary Key)
- username
- email
- password
- phone_number
- role (guest or host)

## Property

- id (Primary Key)
- title
- description
- address
- price_per_night
- owner_id (Foreign Key referencing User)

## Booking
- id (Primary Key)
- user_id (Foreign Key referencing User)
- property_id (Foreign Key referencing Property)
- start_date
- end_date
- total_price

## Review
- id (Primary Key)
- user_id (Foreign Key referencing User)
- property_id (Foreign Key referencing Property)
- rating (e.g., 1-5 stars)
- comment

## Payment
- id (Primary Key)
- booking_id (Foreign Key referencing Booking)
- payment_date
- amount
- payment_method

## Entity Relationships
- A User can own multiple Properties.
- A Property belongs to one User (the host).
- A User can make multiple Bookings.
- A Booking is linked to one User and one Property.
- A Review is written by a User for a Property.
- A Payment is linked to a Booking.

### Feature Breakdown
## User Management
- Users can sign up, log in, and manage their profiles. Hosts can list properties, and guests can book properties. Proper authentication and authorization ensure secure access.
## Property Management
- Hosts can create, update, and delete property listings. Each listing includes details such as location, description, pricing, and images to help guests make informed choices.
## Booking System
- Guests can search for available properties, select dates, and book their stay. The system ensures that bookings are confirmed, and unavailable dates are blocked automatically.
## Review System
- After completing a stay, guests can leave reviews and ratings for properties. This helps maintain quality and trust within the platform.
## Payment Processing
- Secure payment integration allows guests to pay for their bookings online. Payments are linked to bookings, ensuring a smooth transaction for both guests and hosts.
## Search and Filtering
- Guests can search for properties based on location, price range, property type, and other filters. This helps users quickly find properties that match their preferences.
## Admin Panel
- An admin interface is provided for staff members to manage users, properties, bookings, and payments efficiently. This ensures smooth operation and maintenance of the platform.
  
### API Security
## Authentication
- Authentication ensures that only registered users can access the system. It protects the platform by verifying the identity of users before allowing access to user-specific features like bookings and profile management.
## Authorization
- Authorization controls what authenticated users are allowed to do. For example, only hosts can manage properties, and only guests can make bookings. This prevents unauthorized actions and protects sensitive operations.
## Rate Limiting
- Rate limiting restricts how many requests a user can make in a given time. It helps prevent abuse, spam, and protects the server from being overwhelmed by too many requests.
## Data Encryption
- Data transmitted between the client and server will be encrypted. This ensures that sensitive information like passwords and payment details are protected from attackers.

### CI/CD Pipeline
## What is CI/CD?
- Continuous Integration (CI) and Continuous Deployment (CD) are practices that automate the process of integrating code changes into a shared repository and deploying these changes to production. CI ensures that code is tested and integrated regularly, while CD automates the deployment process to make sure updates are delivered efficiently and reliably.
## Importance for the Project
- CI/CD pipelines improve development efficiency, reduce manual errors, and ensure that code is always in a deployable state. By automating the build, test, and deployment processes, teams can deliver new features and bug fixes faster, while maintaining high-quality standards.
## Tools Used for CI/CD
- GitHub Actions: An automation tool that can help us create workflows to build, test, and deploy the code with each commit.
- Docker: Used for creating consistent environments for both development and production, ensuring that the code works uniformly across different platforms.
- Travis CI: An open-source CI/CD service used for automatic testing and deployment of applications.

