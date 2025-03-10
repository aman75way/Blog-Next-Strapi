# Next.js + Strapi Authentication System

## Overview

This project is a **Next.js authentication system** integrated with **Strapi.js** as the backend. It provides user registration, login, and logout functionalities using JWT-based authentication.

## Tech Stack

- **Frontend:** Next.js
- **Backend:** Strapi.js
- **Validation:** Zod
- **Session Management:** HTTP Cookies

## Features

✅ **User Registration**\
✅ **User Login**\
✅ **JWT-based Authentication**\
✅ **Server-side Session Management** (Cookies)\
✅ **Error Handling with Zod Validation**\
✅ **Secure Cookie Storage**

## Installation


### NODE REQUIREMENT
```bash
 node <= 20.0.0
```

### 1. Clone the Repository

```bash
git clone <repo-url>
cd <project-folder>
```

### 2. Install Dependencies

```bash
yarn setup
```

### 3. Seed current data

```bash
yarn seed
```

### 4. Run the Application | BOTH frontend and backend

```bash
yarn dev
```

## Authentication Workflow

1. **User Registration:**

   - Sends `username`, `email`, and `password` to the Strapi backend.
   - Stores the JWT token in **HTTP-only cookies**.

2. **User Login:**

   - Authenticates users using either `email` or `username` with a password.
   - JWT token is received and stored in cookies.

3. **User Logout:**

   - Removes the JWT token by resetting the cookie.

## API Endpoints (Strapi)

| Method | Endpoint                   | Description          |
| ------ | -------------------------- | -------------------- |
| POST   | `/api/auth/local/register` | Registers a new user |
| POST   | `/api/auth/local`          | Logs in a user       |

## Security Best Practices

- Uses **secure, HTTP-only cookies** to store JWT tokens.
- Implements **server-side validation** using Zod.

