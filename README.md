# cab-booking-phase3
Fare Service — Spring Boot Cab Fare App
1. Introduction
Fare Service is a Spring Boot-based microservice that calculates cab fares based on distance and cab type. The project demonstrates the creation of REST APIs, service layers, and a simple HTML interface for testing the service. It is designed for learning and small-scale deployments of microservices.

2. Objectives
•	Develop a RESTful service to calculate fares.
•	Accept input parameters via query strings or an HTML form.
•	Demonstrate proper Spring Boot project structure.
•	Allow easy extension for future cab types or dynamic pricing.
•	Provide an interactive interface for testing without complex front-end frameworks.

3. Features
•	Fare Calculation API: Calculate fare using /fare/calculate endpoint.
•	Test Endpoint: /fare/test confirms service availability.
•	Simple HTML Interface: Input distance and select cab type to get fare.
•	Dynamic Calculation: Supports different cab types (e.g., Sedan, SUV) with configurable rates.

4. Technology Stack
•	Java 21 — Programming language.
•	Spring Boot 3.2.5 — Microservice framework.
•	Maven — Dependency management and build tool.
•	HTML/CSS — Front-end testing page.
•	Eclipse IDE — Development environment.
•	Embedded Tomcat — Web server (default port 8081).

5. Spring Boot Concepts Used
•	REST Controller: Handles HTTP requests and responses.
•	Service Layer: Contains business logic for fare calculation.
•	Dependency Injection: FareController depends on FareService.
•	Request Parameters: Accepts distance and cabType via query string.
•	Embedded Server: Runs on Tomcat without external configuration.
7. How It Works
1.	Run Application: Launch FareService1Application from Eclipse or Maven.
2.	Test Endpoint: Open in browser → http://localhost:8081/fare/test to confirm service is running.
3.	Fare Calculation:
o	URL example:
o	http://localhost:8081/fare/calculate?distance=10&cabType=Sedan
o	Response: 150.0 (calculated fare based on distance and cab type).
4.	HTML Interface: Open index.html in browser for interactive input and output.

8. Installation & Setup
Prerequisites:
•	Java 21 installed.
•	Maven installed.
•	Eclipse IDE (optional).
Steps:
1.	Clone the repository.
2.	Open project in Eclipse.
3.	Update Maven dependencies:
4.	Right-click project → Maven → Update Project
5.	Run Spring Boot application:
6.	Right-click FareService1Application → Run As → Java Application
7.	Access API or HTML page:
o	REST API: http://localhost:8081/fare/calculate?distance=10&cabType=Sedan
o	HTML Page: http://localhost:8081/index.html

Project File Structure
FareService1/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └── example/
│   │   │           └── fareservice1/
│   │   │               ├── FareService1Application.java      // Main Spring Boot application
│   │   │               ├── controller/
│   │   │               │   └── FareController.java           // REST Controller
│   │   │               ├── service/
│   │   │               │   └── FareService.java              // Business logic
│   │   │               └── model/                             // Optional: For DTOs or models
│   │   │                   └── FareResponse.java
│   │   ├── resources/
│   │   │   ├── application.properties                         // Spring Boot configurations
│   │   │   ├── static/                                        // Static files (HTML/CSS/JS)
│   │   │   │   └── index.html                                 // HTML interface for testing
│   │   │   └── templates/                                     // Optional if using Thymeleaf
│   │   └── webapp/                                            // Optional: for more complex front-end
│   └── test/
│       └── java/
│           └── com/
│               └── example/
│                   └── fareservice1/
│                       └── FareService1ApplicationTests.java // Unit tests
├── pom.xml                                                     // Maven configuration
└── README.md                                                   // Project documentation
