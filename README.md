# 📁 File Sharing Management System

A Spring Boot web application that allows users to authenticate via **Google OAuth 2.0** and manage file sharing operations. This project uses **Spring Security**, **MySQL**, and **OAuth 2.0** for secure login.

---

## 🚀 Features

- 🔐 Google Login using OAuth 2.0
- 🗂️ File sharing management system (extensible)
- 🧩 Integrated with MySQL for data persistence
- ✅ Secure authentication using Spring Security
- 🧪 Easy testing with OAuth test users

---

## 🔧 Technologies Used

- Java 17+
- Spring Boot
- Spring Security (OAuth2 Client)
- MySQL
- Maven / Gradle

---

## 📦 Prerequisites

- Java 17+
- MySQL server running on localhost
- Maven or Gradle installed
- Google Cloud Console project

---

## 🌐 Google OAuth Setup

1. Go to [Google Cloud Console](https://console.cloud.google.com/).
2. Create or select a project.
3. Navigate to: `APIs & Services > Credentials`.
4. Click **"Create Credentials" > OAuth Client ID**.
5. Choose **Web application**.
6. Set the **Authorized Redirect URI** as: http://localhost:8080/login/oauth2/code/google

7. Save the **Client ID** and **Client Secret**.

8. Go to `OAuth Consent Screen`:
- Choose **External** user type.
- Fill in App name, support email, and developer contact info.
- Add test users (your Gmail address).
- Save & publish (optional for production).

---

## 🛠️ Configuration

Update your `application.properties`:

```properties
spring.application.name=fileSharingManagement

# Database Config
spring.datasource.url=jdbc:mysql://localhost:3306/Filemanager
spring.datasource.username=root
spring.datasource.password=password
spring.jpa.hibernate.ddl-auto=update

# Logging
logging.level.org.springframework.web=DEBUG

# Google OAuth Config
spring.security.oauth2.client.registration.google.client-id=${google_client_id}
spring.security.oauth2.client.registration.google.client-secret=${google_client_secret}
spring.security.oauth2.client.registration.google.redirect-uri=http://localhost:8080/login/oauth2/code/google

# (Optional) GitHub OAuth Config (if used)
spring.security.oauth2.client.registration.github.client-id=${github_id}
spring.security.oauth2.client.registration.github.client-secret=${github_secret}
```

## Running the App
```bash
./mvnw spring-boot:run
```
Then visit:

```bash
http://localhost:8080/oauth2/authorization/google
```
## TODO
- Add file upload/download features
- Add user dashboard after login
- Deploy to cloud (e.g., Render, Heroku, GCP)

