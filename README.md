# 🏡 Airbnb Clone Project

> *A full-stack, enterprise-level simulation of a modern property booking platform.*

---

## 📘 Overview

The **Airbnb Clone Project** is a project inspired by the real Airbnb platform and is a full-stack web application. This project is designed to enable cologne features and simulate the functionalities of an online property rental platform, Airbnb. This project is aimed to be a practical, and the development can be done in a collaborative manner. It is a widespread presentation of backend architecture, database design, and API development, and how they can be organized in modern software development, how DevOps should be done, and an insight into the security of our applications.

---

## 🎯 Project Goals

- Develop a scalable, secure, and modular **Airbnb-like platform**.
- Master **collaborative team workflows** using GitHub and Agile principles.
- Architect and model **relational databases** mirroring real-world entities.
- Build and secure RESTful and GraphQL **APIs**.
- Design and integrate **CI/CD pipelines** for seamless deployment.
- Utilize **Docker** and container-based environments for development and testing.
- Gain exposure to **end-to-end project lifecycle management**.

---

## 🧰 Technology Stack

| Technology     | Purpose                                                                 |
|----------------|-------------------------------------------------------------------------|
| **Django**     | A high-level Python web framework used to build robust backend systems and RESTful APIs. |
| **Django REST Framework (DRF)** | An extension of Django used to build scalable and secure REST APIs. |
| **GraphQL**    | A query language for APIs enabling efficient data fetching and flexible client-server interactions. |
| **MySQL**      | A relational database management system used to store and manage structured application data. |
| **Docker**     | A containerization platform used to package the application and its dependencies for consistent deployment. |
| **GitHub Actions** | A CI/CD platform to automate testing, building, and deployment of the application. |
| **JWT (JSON Web Tokens)** | Used for stateless, secure authentication and authorization between client and server. |

---

## 👥 Team Roles & Responsibilities

Each team member will contribute under clearly defined roles to simulate real-world software teams:

- **Project Manager** – Oversees timelines, deliverables, and communication.
- **Backend Developer** – Builds and documents the API and business logic.
- **Database Architect** – Designs and manages schema and relationships.
- **DevOps Engineer** – Handles CI/CD, Docker, and deployment automation.
- **QA Engineer** – Ensures system stability, runs tests, and validates functionality.

---

## 🧱 Database Design

### Key Entities & Attributes

1. **User**
   - `id`: Unique identifier
   - `username`: User’s login name
   - `email`: Contact email
   - `password`: Hashed password for authentication
   - `role`: Guest or Host

2. **Property**
   - `id`: Property ID
   - `title`: Name/description of the property
   - `location`: Geographic data
   - `price_per_night`: Cost for one night stay
   - `host`: Foreign key referencing User

3. **Booking**
   - `id`: Booking ID
   - `property`: Foreign key to Property
   - `guest`: Foreign key to User
   - `start_date` / `end_date`: Booking duration
   - `status`: Confirmed, Pending, Cancelled

4. **Review**
   - `id`: Review ID
   - `booking`: Reference to the related booking
   - `rating`: Numerical value (1–5)
   - `comment`: Feedback from the guest
   - `created_at`: Timestamp of review

5. **Payment**
   - `id`: Payment ID
   - `booking`: Linked booking
   - `amount`: Total charged
   - `method`: e.g., card, PayPal
   - `status`: Success, Failed, Pending
     
### Entity Relationships
- A **User** can own multiple **Properties** (host role).
- A **User** can make multiple **Bookings** (guest role).
- A **Booking** belongs to one **Property** and one **User**.
- A **Review** is tied to a **Booking**.
- A **Payment** is linked to one **Booking**.

---

## 🧩 Feature Breakdown

1. **User Management**
   Handles user registration, login, profile updates, and role-based access (guest vs host). It ensures secure identity management across the platform.

2. **Property Management**
   Enables hosts to list properties with details like price, availability, and location. This allows users to browse and interact with available listings.

3. **Booking System**
   Provides functionality for users to book properties, manage dates, and view their reservation history. Integrates with availability logic to prevent double bookings.

4. **Review System**
   Guests can leave ratings and feedback after a stay. This builds community trust and helps others make informed decisions.

5. **Payment Integration**
   Secure processing of payments related to bookings, including receipts and transaction history. Supports multiple methods and ensures financial accountability.

---


## 🔐 API Security

Security is a top-tier priority to protect sensitive user and transactional data.

- **Authentication (JWT)**: Users must log in to receive a token to access protected endpoints. Ensures only authorized access to user-specific data.
- **Authorization**: Role-based access control ensures hosts and guests interact only with the features they’re entitled to use.
- **Rate Limiting**: Prevents abuse of API endpoints by restricting excessive requests, mitigating denial-of-service attacks.
- **Input Validation & Sanitization**: Prevents injection attacks and data corruption by validating all user inputs.
- **HTTPS Enforcement**: Encrypts all client-server communication to protect against man-in-the-middle attacks.

> Without these security layers, user privacy, financial transactions, and platform integrity would be at high risk.

---

## 🔁 CI/CD Pipeline

**CI/CD (Continuous Integration/Continuous Deployment)** automates code testing and deployment, ensuring rapid and reliable software delivery.

- **Why CI/CD?**
   - Automates testing to catch bugs early
   - Speeds up the development cycle
   - Promotes stable, consistent builds and deployments
   - Ensures quality in collaborative environments

- **Tools Used**
   - **GitHub Actions**: Automates workflows on push, pull, or merge events.
   - **Docker**: Creates consistent development and deployment environments.
   - **(Optional)**: Can integrate with platforms like AWS, Heroku, or DigitalOcean for auto-deployment.

---


## 🚀 Getting Started

1. **Clone the repository**  
   ```bash
   git clone https://github.com/Robel-w/airbnb-clone-project.git
   cd airbnb-clone-project
