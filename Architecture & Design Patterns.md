# ⭐ Which architecture is used where?
## 1️⃣ Small Projects (CRUD, simple logic)

Use:
✔ N-Tier (3-Layer) → UI → Business → Data
✔ MVC
✔ Repository Pattern only

Because:

Less code

Faster development

Easy maintainability

👉 Clean, Onion, or DDD would be overkill for small projects.

## 2️⃣ Medium Projects (multiple modules, service integration)


Use:
✔ Clean Architecture
✔ Onion Architecture
✔ CQRS (optional)

Because:

Faster to scale

Better structure

Tests become easier

## 3️⃣ Enterprise / Complex Domain Projects

Use:
✔ DDD (Domain-Driven Design)
✔ Clean + Onion combination
✔ Event-Driven patterns
✔ CQRS + Mediator

Because:

Complex business domain

Entities have deep rules

Bounded contexts

Many modules and integrations

# Examples of Common Patterns Across Architectures

## | Pattern                        | What it Does                                   | Architecture Fit      | Notes                                                                   |
| ------------------------------ | ---------------------------------------------- | --------------------- | ----------------------------------------------------------------------- |
| **Repository**                 | Encapsulates data access                       | Layered, Onion, Clean | In Onion/Clean, often interfaces in core, implementation in outer layer |
| **Unit of Work**               | Groups DB operations into a transaction        | Layered, Onion, Clean | Can be implemented in infrastructure; business logic calls it           |
| **Factory / Abstract Factory** | Creates objects without exposing instantiation | Any                   | In Clean Architecture, factories can live in Application or Core layer  |
| **Singleton**                  | Ensures single instance                        | Any                   | Often in infrastructure (logging, config)                               |
| **Strategy**                   | Allows interchangeable algorithms              | Any                   | In Clean/CQRS, e.g., different validation or calculation strategies     |
| **Command**                    | Encapsulates a request                         | Onion, Clean          | Fits naturally with CQRS                                                |
| **Mediator**                   | Decouples sender and receiver                  | Onion, Clean          | Often used to implement CQRS handlers                                   |
| **Decorator**                  | Adds behavior dynamically                      | Any                   | Example: add caching to repository without changing code                |
| **Observer**                   | Event notification                             | Any                   | Example: domain events in Onion/Clean                                   |

