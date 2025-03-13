# iTravelSolo Backend

## Overview

**iTravelSolo** is a platform designed for solo travelers to connect with like-minded individuals during their trips, fostering new friendships and shared experiences. This repository contains the backend services built with **Java (Spring Boot)** to manage user authentication, trip matching, real-time communication, and recommendations.

## Features

- **User Authentication & Profile Management**: Secure sign-up, login, and profile creation.
- **Trip Planning & Matching**: Users can add their trip details and get matched with similar travelers.
- **Real-time Chat & Notifications**: Enables travelers to connect and chat with their matches.
- **Recommendation System**: Suggests nearby attractions, restaurants, and experiences based on trip details.
- **Admin Panel**: Manages users, reports, and system configurations.

## Tech Stack

- **Backend**: Java (Spring Boot)
- **Database**: PostgreSQL
- **Authentication**: JWT-based authentication
- **Real-time Communication**: WebSockets
- **Cloud Storage**: AWS S3 for media uploads
- **API Documentation**: Swagger
- **Deployment**: Docker, Kubernetes, CI/CD with GitHub Actions

## Getting Started

### Prerequisites

Ensure you have the following installed:

- Java 17+
- Maven
- PostgreSQL
- Docker (optional for containerized deployment)

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/iTravelSolo-backend.git
   cd iTravelSolo-backend
   ```
2. Configure environment variables:
   - Copy `.env.example` to `.env` and update the necessary configurations.
3. Build and run the application:
   ```sh
   mvn clean install
   mvn spring-boot:run
   ```

## API Endpoints

The backend provides RESTful APIs for various functionalities. Below are some key endpoints:

### Authentication

| Method | Endpoint       | Description            |
| ------ | -------------- | ---------------------- |
| POST   | `/auth/signup` | User registration      |
| POST   | `/auth/login`  | User login & JWT token |

### Trips & Matching

| Method | Endpoint         | Description                      |
| ------ | ---------------- | -------------------------------- |
| POST   | `/trips`         | Create a new trip                |
| GET    | `/trips/matches` | Get matched travelers for a trip |

### Chat & Messaging

| Method | Endpoint     | Description               |
| ------ | ------------ | ------------------------- |
| GET    | `/chat/{id}` | Fetch messages for a chat |
| POST   | `/chat/send` | Send a new message        |

Full API documentation is available via Swagger at: `http://localhost:8080/swagger-ui.html`

## Deployment

To deploy using Docker:

```sh
docker build -t itravel-backend .
docker run -p 8080:8080 --env-file .env itravel-backend
```

For Kubernetes deployment, check `k8s/` directory for manifests.

## Contributing

1. Fork the repository
2. Create a new feature branch (`git checkout -b feature-name`)
3. Commit your changes (`git commit -m 'Add feature X'`)
4. Push to the branch (`git push origin feature-name`)
5. Open a Pull Request

## Contact

For queries or contributions, feel free to reach out:

- Email: [prateek0426@gmail.com](mailto\:prateek0426@gmail.com)
- GitHub: pratee-k-umar
- LinkedIn: prateek-kumar-703002252

