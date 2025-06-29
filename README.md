# 🚀 DevBoard – A Full-Stack Developer Task Manager

DevBoard is a modern full-stack task management app inspired by Trello and Jira. It allows developers to manage tasks, collaborate with teams, and track progress efficiently.

Built with:
- **Frontend**: [Next.js 14+ (App Router)](https://nextjs.org)
- **Backend**: [Spring Boot](https://spring.io/projects/spring-boot)
- **Database**: PostgreSQL

---

## 📸 Preview

![DevBoard UI Screenshot](./screenshots/dashboard.png) <!-- Add a real screenshot later -->

---

## 🧱 Tech Stack

| Layer      | Tech Used                            |
|------------|---------------------------------------|
| Frontend   | Next.js, React, TailwindCSS, TypeScript |
| Backend    | Spring Boot, Java, Spring Security, JWT |
| Database   | PostgreSQL, JPA (Hibernate)           |
| Auth       | JWT Token + Cookie-based auth         |
| Dev Tools  | Docker, Vercel, Postman, GitHub Actions (optional) |

---

## 🧠 Features

- 🔐 User authentication (JWT)
- 📦 Create, update, and delete tasks
- 🗃️ Filter and search tasks
- 📂 File uploads (task attachments)
- 🧑‍💻 Admin and user role-based views
- 🌗 Responsive, accessible UI
- 🚀 Deployed frontend & backend

---

## 📁 Project Structure

### 🧩 Frontend – `/frontend` (Next.js)

```
/app
  /auth
    login/page.tsx
    register/page.tsx
  /dashboard
    layout.tsx
    page.tsx
    /tasks
      page.tsx
      [id]/page.tsx
  /components
    TaskCard.tsx
    Header.tsx
  /lib
    api.ts
  layout.tsx
  globals.css
.env.local
```

### 🧩 Backend – `/backend` (Spring Boot)

```
/com/devboard
  /controller
    AuthController.java
    TaskController.java
  /service
    AuthService.java
    TaskService.java
  /model
    User.java
    Task.java
  /repository
    UserRepository.java
    TaskRepository.java
  /dto
    TaskDTO.java
    LoginRequest.java
  /security
    JwtFilter.java
    SecurityConfig.java
application.properties
```

---

## ⚙️ Setup Instructions

### 🔧 Prerequisites

- Node.js 18+
- Java 17+
- PostgreSQL
- (Optional) Docker

---

### 🚀 Run the Frontend (Next.js)

```bash
cd frontend
npm install
npm run dev
```

- Environment:
  ```
  NEXT_PUBLIC_API_URL=http://localhost:8080/api
  ```

---

### 🔧 Run the Backend (Spring Boot)

```bash
cd backend
./mvnw spring-boot:run
```

- PostgreSQL `application.properties` example:

  ```properties
  spring.datasource.url=jdbc:postgresql://localhost:5432/devboard
  spring.datasource.username=your_db_user
  spring.datasource.password=your_db_pass

  spring.jpa.hibernate.ddl-auto=update
  jwt.secret=my-jwt-secret
  ```

---

## 🔐 Authentication Flow

- Register/Login on frontend
- Spring Boot issues JWT token
- Frontend stores token in cookies
- Authenticated requests include JWT for protected routes

---

## 🌐 Deployment

- Frontend → [Vercel](https://vercel.com/)
- Backend → [Render](https://render.com/), Railway, or custom VPS
- PostgreSQL → Hosted DB (Supabase, Neon, or Render)

---

## ✅ TODOs

- [ ] Pagination & sorting
- [ ] OAuth2 login (GitHub/Google)
- [ ] Task comments
- [ ] Notification system (WebSocket or polling)
- [ ] Admin dashboard analytics

---

## 🤝 Contributing

Want to help improve DevBoard? Feel free to open issues, suggest features, or fork and contribute!

---

## 📄 License

This project is licensed under the MIT License.

---

## 🙋‍♂️ Author

Built by [Kunal Chauhan](https://github.com/Kunal-Chauhan7).  
Learning **Next.js**, **Spring Boot**, and building real-world full-stack applications.
