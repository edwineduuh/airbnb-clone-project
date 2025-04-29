# airbnb-clone-project
This project is a  clone of Airbnb, designed to practice by Backend development skills

## Project Goals
- Build a clone version of Airbnb
- Practice advanced backend skills
- Learn teamwork and project management skills

## Tech stack
- Python
- Django
- Basic HTML/CSS
- Javascript
- MySQL

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
- Django: A high-level Python web framework used to build the backend and RESTful APIs of the Airbnb clone.
- MySQL: A relational database used to store user data, property listings, bookings, and other project information.
- GraphQL: A query language for APIs that allows clients to request exactly the data they need, making communication between frontend and backend efficient.
- HTML/CSS: Used to create and style the web pages for the Airbnb clone.
- JavaScript: Adds interactivity to the frontend of the website 

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

