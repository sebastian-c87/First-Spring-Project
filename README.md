# First Spring Project with Thymeleaf

Simple **Spring Boot** application showcasing:
- Basic **Spring MVC** setup
- **Thymeleaf** templating engine
- Serving **static files** (images)
- Passing query parameters to a controller

---

## Overview

This project was generated via [start.spring.io](https://start.spring.io/) using:

- **Maven** (build tool)
- **Java 23**
- **Spring Boot** **3.4.1**
- Dependencies:
  - **Spring Web** (for handling HTTP requests)
  - **Thymeleaf** (server-side template engine)
  - **Lombok** (to reduce boilerplate code)

The application starts an embedded **Tomcat** server on port `8080`.  
It includes a simple controller, `HelloController`, which displays a greeting page (`greeting.html`) using **Thymeleaf**.

---

## Project Structure


- **`FirstSpringProjectApplication`**: Main Spring Boot application class.  
- **`HelloController`**: Contains endpoint mappings.  
- **`greeting.html`**: Thymeleaf template displaying a dynamic greeting and an image.  
- **`application.properties`**: (Optional) config file for Spring Boot.  
- **`vistula.png`**: Static image served from `src/main/resources/static/images`.

---

## How to Run

1. **Clone** or **download** this repository.
2. Make sure you have **Java 17+** installed (we use Java 23 here, but 17 is the minimum for Spring Boot 3.x).
3. In the project directory, run:
   ```bash
   mvn clean package
   mvn spring-boot:run
4. Once the server starts, open http://localhost:8080/greeting?name=Vistula.
You should see a webpage that displays a greeting like "Hello, Vistula!" and the Vistula logo underneath.

## Usage Details

- **Endpoint**: `GET /greeting`  
  - **Query Param**: `name` (e.g., `?name=Vistula`).  
  - **Thymeleaf template**: `greeting.html`  
  - Renders a message and an image (`vistula.png`) from `static/images/`.

Renders "Hello, Vistula!" along with the image in the HTML body.

## About @ResponseBody
Although not explicitly used in this project, @ResponseBody is a Spring annotation that tells the framework to write the return value of a method directly to the HTTP response body.

- This bypasses **Thymeleaf** or any other templating engine and is typically used when creating RESTful endpoints returning JSON or plain text.
- In this application, we’re using **Thymeleaf** templates for rendering HTML views. If we wanted to return raw text or JSON instead, we could use @ResponseBody (or annotate the class with @RestController) to skip view resolution.

---
## Contributing
If you spot any issues or want to add improvements:
1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a Pull Request
All contributions are welcome!
---
---
**License**
This is a simple educational project. You can adapt and reuse the code freely for learning or demonstration purposes.
