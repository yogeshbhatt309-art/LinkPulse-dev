# 🔗 LinkPulse
### Smart Link Management & Analytics Platform

**Developed by Team HLD**

A web-based link management platform designed to simplify URL shortening, link organization, redirection management, and performance tracking through a centralized dashboard.

---

## 🌐 Live Project

**Live Website:** https://lnkpulse-dev.vercel.app/

**Project Name:** LinkPulse  
**Team Name:** Team HLD  
**Project Type:** Web Application  
**Submission:** Hackathon Project

---

## 📌 Problem Statement

Traditional URL shorteners primarily focus on converting long URLs into shorter links. However, modern users require additional capabilities such as link organization, customizable redirects, click tracking, analytics, QR code generation, and security controls.

Managing these functionalities through separate platforms increases complexity and reduces efficiency.

LinkPulse aims to address this problem by bringing essential link-management capabilities together into a unified platform.

## 💡 Our Solution

LinkPulse provides a centralized platform where users can create, manage, organize, and monitor shortened URLs.

The system is designed to offer an intuitive interface alongside backend functionality for authenticated link management, configurable redirection, and click-event tracking.

Our objective is to make link management more accessible, organized, and efficient.

---

## ✨ Project Features

### 1. User Authentication
- User registration and login.
- Authenticated access to link-management features.
- Owner-specific link management.

### 2. URL Shortening
- Generate shortened URLs.
- Create custom link aliases.
- Configure link expiration.
- Set maximum click limits.
- Support password-protected redirects.

### 3. Link Management
- Create and manage shortened links.
- Organize links using campaigns, tags, and folders.
- Enable or disable individual links.
- Configure device-specific destination overrides.

### 4. Analytics and Tracking
- Record link-click events.
- Track timestamps and referrer information.
- Collect basic browser and device information.
- Provide analytics through dashboard and backend endpoints.

### 5. Additional Capabilities
- QR code generation.
- Bio-page functionality.
- Domain blocklist.
- Link creation rate limiting.
- Responsive dashboard interface.

### Project Scope and Limitations

The project focuses on core link-management functionality. Advanced capabilities such as comprehensive geolocation analytics, team workspaces, background click processing, and production-grade bot detection are outside the current implementation scope.

---

## 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Backend | Node.js, Express.js |
| Database | SQLite |
| Authentication | JWT, bcryptjs |
| QR Generation | QRCode |
| Security | Helmet, Express Rate Limit |
| Version Control | Git & GitHub |

---

## 📂 Project Architecture

The application follows a frontend-backend architecture.

**Frontend:** Provides the user interface for creating, organizing, and monitoring links.

**Backend:** Handles authentication, URL generation, redirect rules, analytics, and API requests.

**Database:** Stores application records, user information, link configurations, and click events.

**Security Layer:** Implements authentication, password hashing, request limiting, and link-management restrictions.

---

## ⚙️ Installation and Local Setup

### Prerequisites

Ensure the following are installed:

- Node.js 20 or above
- npm
- Git
- Visual Studio Code (recommended)

### Step 1: Clone the Repository

```bash
git clone https://github.com/USERNAME/team-hld-linkpulse.git
```

Replace `USERNAME` with the actual GitHub account name.

### Step 2: Open the Project

```bash
cd team-hld-linkpulse
```

### Step 3: Install Dependencies

```bash
npm install
```

### Step 4: Configure Environment Variables

Create a `.env` file using `.env.example` as a reference.

**Important:** The application does not automatically load `.env` files. Configure the required environment variables in your shell or deployment environment.

PowerShell example:

```powershell
$env:JWT_SECRET="replace-with-a-unique-random-secret-at-least-32-characters"
npm start
```

Never upload real credentials or secret keys to GitHub.

### Step 5: Run the Application

After configuring the environment, start the application:

```bash
npm start
```

Open your browser and visit:

```text
http://localhost:3000
```

---

## 🚀 Deployment

The application requires a Node.js-compatible hosting environment.

Because the backend uses SQLite, persistent storage is necessary to preserve application data across deployments and restarts.

GitHub Pages alone cannot host the Node.js backend.

For production deployment, configure the required environment variables, provide persistent database storage, and verify all major application workflows.

The provided `render.yaml` illustrates a possible deployment configuration. Persistent hosting may require a paid plan or database migration depending on the selected provider.

---

## 🔒 Security Considerations

LinkPulse incorporates several security-focused mechanisms:

- Password hashing using bcryptjs.
- JWT-based authentication using HTTP-only cookies.
- Request rate limiting.
- Domain blocklisting.
- Link disabling and expiration controls.
- Owner-scoped link management.

These measures provide a foundation for safer link management. Additional security testing and infrastructure improvements would be necessary before large-scale production use.

---

## 🔮 Future Enhancements

The following improvements can be considered for future development:

- Advanced geographical analytics.
- Collaborative team workspaces.
- Enhanced bot detection.
- Background click-event processing.
- Comprehensive automated URL safety scanning.
- Improved analytics visualization.
- Additional integration and customization options.

---

## 🧪 Testing and Demonstration

The core application workflow can be evaluated through the following sequence:

1. Register or log in.
2. Create a shortened URL.
3. Open the generated short link.
4. Verify redirection to the destination.
5. Review recorded click information.
6. Generate a QR code.
7. Disable the link.
8. Verify that the disabled link no longer redirects.

Features should be demonstrated using the actual running application.

---

## 👥 Team Information

**Team Name:** Team HLD  
**Project:** LinkPulse  
**Category:** Web Development / Link Management

The project is developed as part of a hackathon initiative to demonstrate practical web-development skills, problem-solving, backend integration, and application design.

---

## 🎯 Project Objective

Our goal is to develop a practical link-management solution that combines essential URL management features into one accessible platform.

LinkPulse demonstrates how modern web technologies can be integrated to build an organized, functional, and extensible application.

---

**Developed by Team HLD**

*LinkPulse — Simplify Links. Track Performance. Manage Smarter.*
