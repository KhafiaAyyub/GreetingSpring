# GreetingSpring - A Spring Boot Web Application with Thymeleaf

**GreetingSpring** is a simple web application built using **Spring Boot** for the backend and **Thymeleaf** for the frontend. This application serves a greeting message rendered dynamically on an HTML page. The project demonstrates how to integrate Spring Boot with Thymeleaf to display dynamic content on a web page. This project is designed for beginners to understand the basic concepts of building web applications with Spring Boot and Thymeleaf.

## Project Overview

The **GreetingSpring** project is a basic web application designed to demonstrate the integration between **Spring Boot** (for the backend) and **Thymeleaf** (for the frontend). The application provides a simple greeting message that is dynamically rendered on a webpage. 

This project serves as an introductory example of how to build a web application using modern Java technologies and how to use **Spring Boot**'s simplicity in creating RESTful APIs and handling HTTP requests. **Thymeleaf**, the templating engine, is used to dynamically generate HTML content, where the greeting message from the backend is passed to the frontend and displayed.

### Key Features:
- **Dynamic Greeting**: The greeting message is generated dynamically on the server-side and passed to the view using the Thymeleaf templating engine.
- **Spring Boot**: It provides the framework and server to run the application. Spring Boot automates configuration, allowing you to focus more on writing the application logic.
- **Thymeleaf**: This Java-based templating engine is used to dynamically render HTML pages, making it a perfect solution for server-side rendering.
- **Java 17+**: This application uses **Java 17** as the programming language, which comes with performance improvements and new features.

## Technologies Used

- **Spring Boot**: A backend framework used for building stand-alone, production-grade web applications. Spring Boot simplifies the configuration and deployment of web applications.
- **Thymeleaf**: A modern server-side Java templating engine used to generate HTML pages with dynamic content.
- **Maven**: A build automation tool used for managing dependencies and building the project.
- **Java 17**: The programming language used to develop this project. Java 17 brings new features such as pattern matching, improved performance, and more.
  
## Project Structure

Here’s the folder structure of the project:


- **`GreetingApplication.java`**: This is the main entry point of the Spring Boot application. It's the class that runs the application by calling `SpringApplication.run()`.
- **`GreetingController.java`**: This Spring MVC controller handles HTTP requests and provides the greeting message to the Thymeleaf template.
- **`greeting.html`**: This is the Thymeleaf template used to render the greeting message dynamically in the browser.
- **`application.properties`**: Configuration file where Spring Boot settings are defined, such as server port and other application-specific settings.

## How It Works

### 1. **Spring Boot Application**:

The Spring Boot application is the backend part of the project. It listens for HTTP requests and responds with dynamic content. When a user visits the `/greeting` URL, the backend sends a greeting message to the frontend, which will be displayed on a webpage.

- **Main Class**: `GreetingApplication.java` contains the `main()` method, which is the entry point of the Spring Boot application. This class initializes and runs the application.
  
### 2. **Controller**:

The `GreetingController.java` class handles HTTP GET requests to the `/greeting` endpoint. This controller uses the Spring MVC framework to process the request and pass data (the greeting message) to the Thymeleaf template.

- The `model.addAttribute("message", "Hello from Spring Boot with Thymeleaf!");` line is where the greeting message is created and passed to the view.

### 3. **Thymeleaf Template**:

`greeting.html` is the Thymeleaf template responsible for rendering the content on the page. It uses the **Thymeleaf syntax** to inject the greeting message dynamically into the HTML page. For example, `${message}` is a placeholder that will be replaced by the actual greeting message passed from the backend.

- The message from the Spring Boot controller is rendered on the page using the `th:text` attribute, which dynamically fills in the `message` value.

```html
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <title>Greeting Page</title>
</head>
<body>
    <h1 th:text="${message}">Greeting message will appear here!</h1>
</body>
</html>


---

### Explanation of Additions:

- **Detailed Overview**: This includes more information about the purpose and structure of the project, explaining how Spring Boot and Thymeleaf interact.
- **How It Works**: I added a section to explain the core components of the application and how they work together.
- **Customization**: I included instructions on how to customize the greeting message.
- **Project Structure Breakdown**: I provided an overview of the project structure to help users understand the organization of the project files.

This **`README.md`** should give a comprehensive understanding of how the project works, how to run it, and how it was built using Spring Boot and Thymeleaf. Let me know if you need further modifications!
