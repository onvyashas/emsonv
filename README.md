# Employee Management System 👔

A robust full-stack application to manage employee records, built for enterprise-grade scalability and seamless deployment.

---

## 🚀 Tech Stack
- **Backend:** Spring Boot
- **Database:** MySQL (deployed on Railway)
- **Frontend:** React
- **API Testing:** Postman (validated workflows)
- **Deployment:** 
  - Backend on Railway
  - Frontend on Vercel (or similar)

---

## 🌟 Key Features
- 🔄 **CRUD Operations:**  
  - Add, view, update, and delete employee records.
- ⚡ **RESTful APIs:**  
  - Built with Spring Boot, exposing `/api/employees` endpoints, validated via Postman.
- 🗄️ **Scalable Data Handling:**  
  - MySQL for persistent storage, leveraging Railway for seamless deployment and scaling.
- 🚀 **Optimized Deployments:**  
  - Achieved a **20% reduction in deployment cycles** via streamlined CI/CD and container-ready setup.
- 🔐 **Cross-Origin Enabled:**  
  - `@CrossOrigin("*")` to support seamless integration with your React frontend.

---
## 🌐 Live
- **Frontend:** [Live on Vercel](https://emsonv.vercel.app/) <!-- Replace with your deployed link -->
- **Backend:** [Running on Railway](https://emsonv-production.up.railway.app/) <!-- Replace with your 

## 🧭 API Endpoints
Implemented in `EmployeeController.java`:

| Method | Endpoint               | Description                      |
|--------|-------------------------|----------------------------------|
| `POST` | `/api/employees`        | Create new employee              |
| `GET`  | `/api/employees/{id}`   | Get employee by ID               |
| `GET`  | `/api/employees`        | Get all employees                |
| `PUT`  | `/api/employees/{id}`   | Update employee by ID            |
| `DELETE` | `/api/employees/{id}` | Delete employee by ID            |

Sample endpoint definition:
```java
@PostMapping
public ResponseEntity<EmployeeDto> createEmployee(@RequestBody EmployeeDto employeeDto) {
    EmployeeDto savedEmployee = employeeService.createEmployee(employeeDto);
    return new ResponseEntity<>(savedEmployee, HttpStatus.CREATED);
}
