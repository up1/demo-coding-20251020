# Copilot Instructions for .NET 8+ REST API Projects

This repository contains .NET applications. When generating code, please follow these guidelines:

1. **Project Structure**: Adhere to the standard ASP.NET Core project structure. Place controllers in the `Controllers` folder, services in the `Services` folder, repositories in the `Repositories` folder, and entities/models in the `Models` folder. Use DTOs in a `DTOs` folder for data transfer objects.

2. **Attributes**: Use appropriate .NET attributes such as `[ApiController]`, `[Route]`, `[HttpGet]`, `[HttpPost]`, `[HttpPut]`, `[HttpDelete]` to define API endpoints and routing.

3. **Dependency Injection**: Utilize .NET's built-in dependency injection. Register services in `Program.cs` using `builder.Services`. Prefer constructor injection for better testability. Use appropriate service lifetimes: `AddScoped`, `AddTransient`, or `AddSingleton`.

4. **Configuration**: Use `appsettings.json` and `appsettings.Development.json` for configuration settings. Leverage the Options pattern with strongly-typed configuration classes. Avoid hardcoding values in the code.

5. **Error Handling**: Implement global exception handling using middleware or exception filters. Create custom exception classes and use `ProblemDetails` for consistent error responses following RFC 7807.

6. **RESTful Practices**: Follow RESTful principles for API design, including proper use of HTTP methods (GET, POST, PUT, DELETE, PATCH) and status codes. Return `IActionResult` or `ActionResult<T>` from controller actions for flexibility.

7. **Testing**: Write unit tests using xUnit, NUnit, or MSTest with Moq or NSubstitute for mocking. For integration tests, use `WebApplicationFactory<TProgram>` with `Microsoft.AspNetCore.Mvc.Testing`.

8. **Logging**: Use `ILogger<T>` with the built-in logging framework. Configure logging providers in `appsettings.json`. Avoid using `Console.WriteLine` for logging purposes. Use structured logging with log levels appropriately.

9. **Security**: Implement security features using ASP.NET Core Identity or JWT authentication. Use `[Authorize]` and `[AllowAnonymous]` attributes. Follow best practices for authentication and authorization. Implement CORS policies as needed.

10. **Documentation**: Use Swashbuckle (Swagger) for API documentation. Add XML documentation comments to controllers and models. Ensure that all endpoints are well-documented with summary, remarks, and response types.

11. **Database Access**: Use Entity Framework Core for database interactions. Define DbContext classes and entity models. Use repositories pattern or direct DbContext injection. Apply migrations for schema management.

12. **Asynchronous Processing**: Use `async`/`await` pattern for I/O-bound operations. Return `Task` or `Task<T>` from asynchronous methods. For background tasks, use `IHostedService` or `BackgroundService`.

13. **Caching**: Implement caching using `IMemoryCache` for in-memory caching or `IDistributedCache` for distributed caching (Redis). Use response caching middleware where appropriate to improve performance.

14. **Validation**: Use Data Annotations or FluentValidation for model validation. Leverage `[ApiController]` attribute for automatic model state validation.

15. **Middleware**: Create custom middleware for cross-cutting concerns. Chain middleware appropriately in the request pipeline in `Program.cs`.

16. **API Versioning**: Implement API versioning using `Microsoft.AspNetCore.Mvc.Versioning` to maintain backward compatibility.

17. **Performance**: Use minimal APIs for lightweight endpoints. Implement pagination for large datasets. Use `IAsyncEnumerable<T>` for streaming large result sets.

By adhering to these guidelines, you will maintain consistency, security, and quality across the .NET REST API projects in this repository.

