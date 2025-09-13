## ASP .NET CORE (Notes)

### This was from a different video which only has MVC tutorial

<details>
<summary>05 September 2025</summary>
 
## What is ASP.NET Core?
- A framework built by Microsoft to create web applications.  
- Runs on **C#**.  
- **Advantages**:  
  - Cross-platform  
  - High performance  
  - Open-source  

---

## Approaches/Patterns in ASP.NET Core
- MVC (Model-View-Controller)  
- Web API  
- Razor Pages  
- Blazor  

---

## MVC (Model-View-Controller)

MVC is one of the patterns/approaches of ASP.NET Core to build applications.  

### Components
1. **Model** – Represents the shape of data.  
2. **View** – Represents the user interface.  
3. **Controller** – Handles user requests and acts as an interface between Model & View.  

### Web App Configuration
Two aspects:
1. Add services to the container  
2. Configure request pipeline  

---

## MVC Architecture

<img width="858" height="440" alt="image" src="https://github.com/user-attachments/assets/a62c56c7-8afe-454f-b332-b90dd28540f3" />

## Routing in MVC

The URL pattern for routing is considered after the domain name.

Example:
```
https://localhost:55555/Category/Index/3
```
Domain name → localhost:55555
Controller → Category
Action → Index
Id → 3

## Important Notes
### SSL & TLS SSL (Secure Socket Layer – Old) TLS (Transport Layer Security – New)

Used for encrypted communication between browser & website. When using HTTPS, browsers expect valid SSL/TLS certificates.

#### Certificates
- Real sites → Buy valid certificates.
- Localhost → Use self-signed or invalid certificates → usually gives error:

ERR_CERT_INVALID

To bypass in development:
```
dotnet dev-certs https --trust
```

### Ports

Example:
```
http://localhost:12345/
```

localhost → machine/server
12345 → port number (represents a service)
At different ports → different services/apps can run.

Hosting
In production hosting, ports are usually hidden using Reverse Proxy.


    http://app.com/api --> reverse proxy --> http://app.com:5024/


Default Ports
HTTP → 80
HTTPS → 443

Reverse Proxy
Server-level routing is done by:
Nginx
Apache
IIS

</details>


### This is from  video (ASP NET Core Tutorial)[https://www.youtube.com/watch?v=4IgC2Q5-yDE&list=PL6n9fhu94yhVkdrusLaQsfERmL_Jh4XmU]

<details>

 <summary>13 September 2025</summary>

# ASP.NET Core

It is a **.NET Core framework** for building modern, cloud-based, and internet-connected applications.

---

## Features

### (i) Cross Platform
- It can be developed and run on different platforms like:
  - Windows  
  - macOS  
  - Linux  

- It can be hosted on:
  - IIS  
  - Kestrel  
  - Docker  
  - Self-host in your own process  

---

### (ii) Unified Programming Model for MVC & Web API
- Both MVC & Web API controller classes use the same **Controller** base class.  
- They return `IActionResult` interface.  

IActionResult
├── ViewResult
└── JsonResult


---

### (iii) Dependency Injection
- Built-in support for DI.

---

### (iv) Testability
- Provides better testability for apps.

---

### (v) Open Source
- Entirely open source and community-driven.

---

### (vi) Modularity (Modular)
- Provides modularity using **middleware components**.  
- Both request & response pipelines are composed of middleware.  
- Rich set of middleware components provided out of the box.  
- Custom middleware components can also be created.  

---

## ASP.NET Core Templates

ASP.NET Core
├── Empty
├── Web API
├── Web App (MVC)
├── Web App (Blazor)
├── Web App (Razor Pages)
└── Class Library

---

## ASP.NET Core Project File

- `.csproj` or `.vbproj` depending on language.  
- No need to unload project to access project file.  
- File or folder references are no longer included in project file.  
- The **file system** determines what files & folders belong to the project.  

---

## Target Framework

- Defines which API or SDK the project supports.  
- Defined using **Target Framework Moniker (TFM)**.  

Example:  

```xml
<TargetFramework>net9.0</TargetFramework>

```

# ASP.NET Core Hosting Model

Specifies how the apps should be hosted:

## InProcess
- Hosts the app inside of **IIS worker process** (`w3wp.exe`).

## OutOfProcess
- Forwards web requests to backend ASP.NET Core app running the **Kestrel server**.  
- **Default mode** is **OutOfProcess**.

---

# Package Reference

- Used to include a reference to a **NuGet package** that is installed in the app.  
- Example metapackage: `Microsoft.AspNetCore.App`.  
- A metapackage does not have content of its own.  
- It just contains a list of dependencies (other packages).  
- If version is not specified, an **implicit version** is specified by the SDK.  
- Prefer implicit versioning instead of explicitly setting version numbers.  

 
</details>
