# AuthX: Java-Based Authentication & Authorization Framework

AuthX is a **Java-based framework** designed to provide secure **authentication and authorization** using **software design patterns**.  
The goal of this project is to build a **modular, reusable, and extensible security framework** for modern applications.

---

## 🔹 Features
- **Authentication Strategies**
  - Basic username-password login
  - Multi-Factor Authentication (MFA) with OTP
- **Authorization**
  - Role-Based Access Control (RBAC) – separate access for Admin, User, etc.
- **Session Management**
  - Managed using the **Singleton** pattern
- **UI Customization**
  - Light/Dark mode styling with **Decorator** pattern
- **Design Pattern Integration**
  - Strategy, Factory, Singleton, and Decorator patterns for clean architecture

---

## 🔹 Project Structure
- `IAuthStrategy` → Interface for authentication strategies  
- `BasicAuth`, `MFAAuth` → Implementations of login strategies  
- `AuthFactory` → Factory class for creating strategy objects  
- `SessionManager` → Singleton class to manage login sessions  
- `ComponentDecorator` → Enhances UI dynamically  

---

## 🔹 Example Code
```java
// Strategy Interface
public interface IAuth {
    public String createComponent();
}

// Concrete Strategy - Basic Authentication
public class BasicAuth implements IAuth {
    @Override
    public String createComponent() {
        return "ComponentString";
    }
}

// Concrete Strategy - MFA Authentication
public class MFAAuth implements IAuth {
    @Override
    public String createComponent() {
        return "ComponentStringWithOTP";
    }
}
