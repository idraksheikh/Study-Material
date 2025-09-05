## ASP .NET CORE (Notes)

<details>
<summary>05 September 2025</summary>
 
# ASP.NET Core (MVC)

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

```mermaid
flowchart LR
    User[User (Actor)] -->|1. Request| Controller
    Controller -->|2. Get data| Model
    Model --> Controller
    Controller -->|3. Get presentation| View
    View -->|4. Response| User

</details>
