# 📚 Spring School Management System

An enterprise-grade **Java Spring Boot** web application for managing school operations, built with a layered **MVC architecture**, **Spring Security**, and **MySQL**. The system supports multiple user roles (Admin, Student, Guest), delivering functionality for profile management, course enrollment, job applications, holiday tracking, and real-time admin-student communication.

---

## 🚀 Tech Stack

| Category              | Tools & Frameworks                                                             |
|-----------------------|---------------------------------------------------------------------------------|
| Backend               | Java, Spring Boot, Spring MVC, Spring Security, Spring Data JPA, Hibernate     |
| Frontend              | HTML5, CSS3, Bootstrap, Thymeleaf                                              |
| Database              | MySQL (with JPA ORM & Hibernate)                                               |
| Build & Deployment    | Maven, Apache Tomcat                                                           |
| Utilities & Libraries | Lombok, Spring Mail, JPA Auditing                                              |
| Security              | Role-Based Access Control, Form Authentication                                 |
| Tools                 | Git, GitHub                                                                    |

---

## 🌟 Features

### 👨‍🏫 **Admin Panel**
- View and manage **Contact Us** messages from users; close resolved tickets.
- Review, **shortlist, hire, or reject** job applicants with automated email notifications.
- Create and assign **classes**; add students based on email lookup.
- Create and manage **courses** (title, description, lessons, price, preview image).
- View enrolled students per course with real-time tracking.
- Maintain **holiday calendars** and synchronize them for student views.

### 👨‍🎓 **Student Dashboard**
- Login securely and view a **custom dashboard**.
- Update personal details (name, email, address, mobile number).
- Enroll/unenroll in available courses.
- Track upcoming **school holidays** and view current class assignment.

### 🌐 **Public/Guest Access**
- Visit website pages: **About Us**, **Contact**, and **Careers**.
- Register or login to the system.
- Reset forgotten passwords via a secure reset email workflow.
- Apply for jobs using the online career portal.

---

## 🔐 Authentication & Security

- Implements **Spring Security** for user authentication.
- Role-based access for Admin and Student with protected page access.
- HTML view-level access control using Thymeleaf + Spring Security integration.
- CSRF protection and input validation using Spring Boot's validation annotations.

---

## 🗂️ Project Structure

```
src/
│
├── controller/         # Handles web page routing and form submissions
├── model/              # Entity classes (User, Course, Class, Holiday, etc.)
├── repository/         # JPA Repositories for DB access
├── service/            # Business logic
├── security/           # Spring Security configuration
├── templates/          # Thymeleaf-based frontend templates
├── static/             # Static assets like CSS/JS/images
└── application.properties  # DB config, mail server config
```

---

## 💾 Database Schema Diagram

![Database Schema](https://user-images.githubusercontent.com/33577947/180804066-a2dbb8fb-ad1c-4992-af1b-73b9462402a4.png)

---

## 🛠️ Getting Started (Local Setup)

### 🧑‍💻 Prerequisites

- Java 17+
- Maven
- MySQL Server
- IDE (IntelliJ or Eclipse recommended)

### ⚙️ Configuration

Update `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/spring_school
spring.datasource.username=yourUsername
spring.datasource.password=yourPassword

spring.jpa.hibernate.ddl-auto=update
spring.mail.host=smtp.example.com
spring.mail.username=you@example.com
spring.mail.password=yourPassword
```

### 🔧 Build & Run

```bash
# Compile and install dependencies
mvn clean install

# Run the application
mvn spring-boot:run
```

Access at: `http://localhost:8080`

---

## 📤 Deployment Notes

- Built-in support for deployment on **Apache Tomcat**.
- Adaptable for deployment on **Heroku**, **AWS Elastic Beanstalk**, or **Docker**.
- File uploads (images, PDFs) are currently saved in local folders. For cloud compatibility, update to use **AWS S3** or **Firebase Storage**.

---

## 📈 Key Highlights

- 🔐 Secure login with Spring Security
- 📨 Real-time job application emails via Spring Mail
- 📋 Dynamic forms with server-side validation
- 📚 Role-based navigation: Admin vs Student
- 🧠 Clean separation of concerns (MVC Pattern)
- 💬 Ticketing system for support queries
- 🗓️ Real-time holiday and class syncing
- 🕵️ JPA Auditing for entity tracking (Created By, Updated Date, etc.)

---

## 🤝 Contributing

Feel free to contribute new modules, fix bugs, or suggest ideas!

```bash
git clone https://github.com/Vkartik-3/spring-school-portal.git
cd spring-school-portal
# Create a branch and commit your changes
```

---

## 📄 License

This project is licensed under the MIT License.

---

### 👨‍💻 Maintained by [Kartik Vadhawana](https://github.com/Vkartik-3)
