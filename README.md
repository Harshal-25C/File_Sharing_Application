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
6. Set the **Authorized Redirect URI** as:

