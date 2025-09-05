## ASP .NET CORE (Notes)

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

flowchart LR
    A[http://api.com/api] -- reverse proxy --> B[http://app.com:5024/]


Default Ports
HTTP → 80
HTTPS → 443

Reverse Proxy
Server-level routing is done by:
Nginx
Apache
IIS

</details>
