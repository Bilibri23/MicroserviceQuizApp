# Quiz Microservice Application

## Overview

This project demonstrates the implementation of a microservices architecture by building a Quiz application. Each service within the application is independent, ensuring loose coupling and scalability.

### Technologies/services  Used

- Spring Boot: Framework for building Java-based applications
- Postman: API testing client
- PostgreSQL: Database for storing data
- Eureka Server: Service registry for managing service instances
- OpenFeign: Declarative REST client for making HTTP requests
- API Gateway: Intermediary between clients and microservices

## Application Overview

### Services

1. Quiz Service
    - Sends HTTP requests to the Question Service without directly interacting with the question database.
    - Processes responses submitted by the user and returns their score.
    
2. Question Service
    - Handles CRUD operations for quiz questions.
    - Provides questions to the Quiz Service.

### Service Communication

- Eureka Server: Registers and discovers different services.
- OpenFeign: Used by the Quiz Service to communicate with the Question Service.
- API Gateway: Acts as an intermediary between the client and various services.

## Flow of the Application

1. Quiz Service:
    - Retrieves questions from the Question Service via HTTP requests.
    - Processes user responses.
    - Computes and returns the user's score.

2. Question Service:
    - Manages the question database.
    - Provides CRUD operations for questions.
    - Supplies questions to the Quiz Service upon request.

## Repository Links

- [Quiz Service](https://github.com/Bilibri23/QuizService.git)
- [Question Service](https://github.com/Bilibri23/QuestionService.git)
- [Eureka Server](https://github.com/Bilibri23/Service-registry.git)
- [API Gateway](https://github.com/Bilibri23/api-gateway.git)

## Getting Started

### Prerequisites

- JDK 17 or higher
- PostgreSQL
- Postman
- Maven


Set up the databases:
    - Configure PostgreSQL with the necessary databases for the Quiz and Question Services.

### Testing the Application

- Use Postman to test the endpoints exposed by the API Gateway.
- You can perform CRUD operations on the questions via the Question Service.
- You can submit quiz responses via the Quiz Service and receive the score.

## Contributing

1. Fork the repository
2. Create your feature branch (git checkout -b feature/AmazingFeature)
3. Commit your changes (git commit -m 'Add some AmazingFeature')
4. Push to the branch (git push origin feature/AmazingFeature)
5. Open a pull request

## License

Distributed under the MIT License. See LICENSE for more information.

---

This project is a practical example of how to build a microservices architecture with Spring Boot, Eureka, and API Gateway. Each service is designed to be independently deployable and scalable, demonstrating the benefits of a microservices approach.
 
