# dot-net-core-interview-questions-answers

**1: What is the .NET Framework?**

Ans

The .NET is a Framework, which is a collection of classes of reusable libraries given by Microsoft to be used in other .NET applications and to develop, build and deploy many types of applications on the Windows platform including the following:

- Console Applications
- Windows Forms Applications
- Windows Presentation Foundation (WPF) Applications
- Web Applications
- Web Services
- Windows Services
- Services-oriented applications using Windows Communications Foundation (WCF)
- Workflow-enabled applications using Windows Workflow Foundation(WF)

**2.What is .Net Core ? Can you explain core feature of it ?**

Ans

.NET Core is an open-source, cross-platform framework developed by Microsoft for building various types of applications, including web applications, services, and command-line tools. It's a successor to the .NET Framework and provides several advantages over its predecessor, including improved performance, better modularity, and broader platform support.

Some core features of .NET Core include:

- _Cross-Platform_ _Support_: .NET Core is designed to run on multiple platforms, including Windows, macOS, and various distributions of Linux. This allows developers to write code once and run it on different operating systems without modification.

_High_ _Performance_: .NET Core offers significant performance improvements over the traditional .NET Framework, thanks to various optimizations and enhancements. It includes features like just-in-time (JIT) compilation, which compiles code into native machine instructions at runtime for faster execution.

_Modularity_: .NET Core is built with modularity in mind, allowing developers to include only the necessary components in their applications. This helps reduce the size of the application and improve its performance.

_Command-Line_ _Tools_: .NET Core provides a set of command-line tools that streamline various development tasks, such as project creation, building, testing, and deployment. These tools are platform-agnostic and can be used across different operating systems.

_Unified_ _API_: .NET Core provides a unified API surface across different platforms, ensuring consistent behavior and reducing compatibility issues when targeting multiple environments.

_Open-Source_: .NET Core is fully open-source, meaning that its source code is publicly available and can be freely modified and distributed. This allows the community to contribute improvements, fix bugs, and add new features to the framework.

_Support_ _for_ _Modern_ _Workloads_: .NET Core is well-suited for building modern cloud-native applications, microservices, and containerized workloads. It provides integration with popular tools and frameworks used in modern development, such as Docker, Kubernetes, and Azure services.


**2. What is difference between .Net and .Net Core ? Advantages on .Net Core over .Net? 

Ans
- Architecture:
    - Traditional .NET Framework is a Windows-only framework that primarily targets Windows-based applications. It relies on the Windows operating system.
    - .NET Core is a cross-platform framework that can run on Windows, Linux, and macOS. It's designed for modern, cloud-based applications.
- Cross-Platform Support:
    - .NET had limited cross-platform support. Historically, .NET Framework was tightly coupled with Windows.
    - NET Core has built from the ground up with cross-platform support. This allows developers to write applications that can run on multiple operating systems, increasing flexibility and scalability.
- Performance:
    - While in .NET performance has improved over the years, .NET Framework can be slower compared to .NET Core, especially in high-performance scenarios.
    - NET Core designed with performance in mind. .NET Core offers significant performance improvements over .NET Framework, especially for web applications and microservices.
        - _Optimized_ _Runtime_ :.NET Core has a redesigned, modular runtime that's optimized for performance. It includes features such as tiered compilation, which compiles frequently executed code paths to native code for faster execution.
        - _Just_-_in_-_Time_ _(JIT)_ _Compilation_:.NET Core's JIT compiler has been improved to generate more efficient machine code, leading to better runtime performance. It can take advantage of modern CPU architectures and optimizations.
        - _Concurrency_ _and_ _Parallelism_ : .NET Core provides improved support for concurrency and parallelism, allowing applications to take full advantage of multi-core processors. This can lead to significant performance gains, especially for compute-intensive workloads.
- Deployment:
    - Deployment of .NET Framework applications often involves complex dependencies and configurations, making it challenging to deploy consistently across different environments.
    - NET Core: Designed with performance in mind, .NET Core offers significant performance improvements over .NET Framework, especially for web applications and microservices.

        - _Self-contained_ _Deployments_ :With .NET Core, you can create self-contained deployments where all the necessary dependencies, including the .NET Core runtime, are included with the application. This eliminates the need for the target machine to have the runtime installed, simplifying deployment and ensuring that the application runs consistently across different environments.
        - _Side-by-Side_ _Versioning_ : .NET Core allows multiple versions of the runtime to be installed side-by-side on the same machine. This means you can deploy applications with specific runtime dependencies without worrying about conflicts with other applications or system-wide configurations. Each application can specify its required runtime version, ensuring compatibility and reducing deployment issues.
        - _Portable_ _Binaries_ : .NET Core applications can be compiled into portable binaries that are platform-agnostic. This means you can build and package your application on one platform (e.g., Windows) and deploy it to another platform (e.g., Linux) without modification. This simplifies deployment across different operating systems and reduces the effort required to manage platform-specific configurations.
        - _Docker_ _Support_ :er Support: .NET Core has excellent support for Docker containers, allowing you to package your application and its dependencies into lightweight, portable containers. Docker containers provide a consistent runtime environment across different infrastructure platforms, making deployment more predictable and scalable. Additionally, Docker's tooling and ecosystem simplify tasks such as building, distributing, and orchestrating containerized applications.
        - _Integration_ _with_ _CI/CD_ _Pipelines_:.NET Core integrates seamlessly with continuous integration and continuous deployment (CI/CD) pipelines. You can use popular CI/CD tools such as Azure DevOps, Jenkins, and GitHub Actions to automate the build, test, and deployment process for your .NET Core applications. This streamlines the deployment workflow and enables rapid delivery of updates to production environments.
- Open-Source and Community Support:
    - .NET: Historically, .NET Framework was primarily developed by Microsoft with limited community involvement.
    - .NET Core: Developed as an open-source project with contributions from both Microsoft and the community. This fosters a more vibrant ecosystem with rapid development and innovation.
- Modularity and Lightweight:
    - .NET: Monolithic framework with a large footprint due to extensive libraries and dependencies
    - .NET Core: Modular framework with a smaller footprint, allowing developers to include only the necessary components in their applications. This results in smaller container sizes and faster startup times, making it ideal for microservices architecture and containerized deployments.
deployments.
- Support for Modern Development Practices:
    - .NET: Limited support for modern development practices like containerization, serverless computing, and microservices architecture.
    - .NET Core: Built with modern development practices in mind, .NET Core seamlessly integrates with container orchestrators like Kubernetes, supports serverless computing models, and is optimized for microservices architecture


**3. What is Application Domain (AppDomain) in .NET ?**

Ans: https://learn.microsoft.com/en-us/dotnet/framework/app-domains/application-domains

In the context of the .NET framework, an "application domain" (often abbreviated as "AppDomain") is a lightweight process that serves as an isolated environment in which applications run. It provides a level of isolation, security, and control over the execution of managed code within a process. Each .NET application typically runs within its own application domain.

Here are some key points about application domains:

- _Isolation_: Application domains provide a level of isolation between applications running within the same process. This isolation helps prevent faults or exceptions in one application from affecting others.

- _Security_: AppDomains can be configured with different security policies, allowing administrators to control the permissions and resources available to the code running within each domain.

- _Resource_ _Management_: They allow for efficient resource management within a process. Resources such as memory, threads, and file handles can be allocated and managed independently for each application domain.

- _Unloadability_: Application domains can be unloaded independently, allowing for the dynamic loading and unloading of components within a running process without affecting other components.

- _Versioning_: They can help with versioning and updating of components. Different versions of assemblies can be loaded into separate application domains within the same process, allowing multiple versions to coexist without conflicts.

Overall, application domains provide a flexible and secure way to host and manage multiple .NET applications within a single process, enhancing the scalability, reliability, and security of .NET applications.


**3. Explain Middle Ware in .Net Core ?**

Ans

-In ASP.NET Core, middleware components are software components that are added to the application pipeline to handle requests and responses. 
- Middleware sits between the client and the server and can perform various tasks such as authentication, logging, error handling, etc. 
- Middleware components are executed in the order they are added to the pipeline, and each component can choose to pass the request to the next middleware or terminate the request.

Here's an example of a custom middleware in ASP.NET Core:
```
using Microsoft.AspNetCore.Builder;
using Microsoft.AspNetCore.Http;
using System;
using System.Threading.Tasks;

public class CustomMiddleware
{
    private readonly RequestDelegate _next;

    public CustomMiddleware(RequestDelegate next)
    {
        _next = next;
    }

    public async Task InvokeAsync(HttpContext context)
    {
        // Do something before the request reaches the next middleware
        Console.WriteLine("CustomMiddleware executing before the next middleware.");

        // Call the next middleware in the pipeline
        await _next(context);

        // Do something after the request has been processed by the next middleware
        Console.WriteLine("CustomMiddleware executing after the next middleware.");
    }
}

public static class CustomMiddlewareExtensions
{
    public static IApplicationBuilder UseCustomMiddleware(this IApplicationBuilder builder)
    {
        return builder.UseMiddleware<CustomMiddleware>();
    }
}

```
    - In this example, _'CustomMiddleware'_ is a custom middleware component. It contains an _InvokeAsync_ method that accepts an _HttpContext_ object and a _RequestDelegate_ representing the next middleware in the pipeline. 
    - Inside the _'InvokeAsync'_ method, you can execute code before and after calling the _next_ middleware using the _next delegate.

To use this middleware in your ASP.NET Core application, you need to add it to the application pipeline in the Configure method of the Startup class:
```
public class Startup
{
    public void Configure(IApplicationBuilder app)
    {
        app.UseCustomMiddleware();

        // Other middleware configurations
    }
}

```
Now, whenever a request is made to your ASP.NET Core application, it will pass through the CustomMiddleware, and you can execute custom code before and after each request is processed by other middleware components in the pipeline.












