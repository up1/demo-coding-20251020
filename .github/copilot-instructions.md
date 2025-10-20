# Copilot Instructions for Spring Boot Projects

This repository contains Spring Boot applications. When generating code, please follow these guidelines:
1. **Project Structure**: Adhere to the standard Spring Boot project structure. Place controllers in the `controller` package, services in the `service` package, repositories in the `repository` package, and entities in the `model` package.
2. **Annotations**: Use appropriate Spring annotations such as `@RestController`, `@Service`, `@Repository`, and `@Entity` to define components.
3. **Dependency Injection**: Utilize Spring's dependency injection features. Prefer constructor injection over field injection for better testability.
4. **Configuration**: Use `application.properties` or `application.yml` for configuration settings. Avoid hardcoding values in the code.
5. **Error Handling**: Implement global exception handling using `@ControllerAdvice` and custom exception classes.
6. **RESTful Practices**: Follow RESTful principles for API design, including proper use of HTTP methods (GET, POST, PUT, DELETE) and status codes.
7. **Testing**: Write unit tests using JUnit and Mockito. For integration tests, use Spring's testing support with `@SpringBootTest`.
8. **Logging**: Use SLF4J with Logback for logging. Avoid using `System.out.println` for logging purposes.
9. **Security**: If applicable, implement security features using Spring Security, following best practices for authentication and authorization.
10. **Documentation**: Use Swagger/OpenAPI for API documentation. Ensure that all endpoints are well-documented.
By following these guidelines, you will help maintain consistency and quality across the Spring Boot projects in this repository.
11. **Database Access**: Use Spring Data JPA for database interactions. Define repositories as interfaces extending `JpaRepository` or `CrudRepository`.
12. **Asynchronous Processing**: For tasks that can be performed asynchronously, use `@Async` annotation and configure an appropriate task executor.
13. **Caching**: Implement caching using Spring Cache abstraction where necessary to improve performance.


By adhering to these additional guidelines, you will further enhance the maintainability and scalability of the Spring Boot projects in this repository.

