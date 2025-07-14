# CustomFlorist Backend

CustomFlorist is a backend service for a customizable florist application, built with Spring Boot. It provides APIs for managing bouquets, flowers, orders, payments, user authentication, statistics, and more. The project is designed for extensibility and secure, modern web development.

## Features

- User authentication and authorization (JWT, OAuth2)
- Bouquet and flower management
- Order and payment processing (VNPay integration)
- Monthly statistics and product analytics
- Email notifications
- RESTful API with OpenAPI/Swagger documentation
- MySQL database integration
- Docker support for easy deployment

## Tech Stack

- Java 17
- Spring Boot 3.x
- Spring Data JPA
- Spring Security
- MySQL
- Lombok
- Swagger/OpenAPI
- Docker

## Getting Started

### Prerequisites

- Java 17+
- Maven 3.6+
- MySQL

### Clone the Repository

```bash
git clone <your-repo-url>
cd Web_Custom_Florist_BE
```

### Configuration

Edit `src/main/resources/application.yml` or set the following environment variables as needed:

- `DBMS_CONNECTION` (default: jdbc:mysql://localhost:3306/swd392_custom_florist)
- `DBMS_USERNAME` (default: root)
- `DBMS_PASSWORD` (default: 123456)
- `JWT_SECRET_KEY`
- `GOOGLE_OAUTH2_CLIENT_ID`, `GOOGLE_OAUTH2_CLIENT_SECRET`
- `MAIL_HOST`, `MAIL_PORT`, `MAIL_USERNAME`, `MAIL_PASSWORD`
- `VNPAY_TMN_CODE`, `VNPAY_SECRET_KEY`

### Build and Run (Maven)

```bash
mvn clean install
mvn spring-boot:run
```

Or run the packaged JAR:

```bash
java -jar target/*.jar
```

### Run with Docker

Build and start the container:

```bash
docker build -t customflorist-backend .
docker run -p 8080:8080 --env-file .env customflorist-backend
```

### API Documentation

After starting the application, access the Swagger UI for API documentation at:

```
http://localhost:8080/swagger-ui/index.html
```

## License

This project is for educational/demo purposes. See the source for details.
