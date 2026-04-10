# Secure MERN Authentication Prototype

This project is a modular MERN stack authentication prototype with secure registration, image-based CAPTCHA, multi-factor authentication using Microsoft Authenticator, JWT-based login, and role-based home access.

## Project structure

- `backend/` — Node.js + Express API
- `frontend/` — React + Vite user interface

## Features

- Secure password policy matching NIST-style recommendations
- CAPTCHA generation for bot protection
- MFA setup using TOTP and QR codes
- JWT authentication for protected endpoints
- Role-based access control for admin, manager, and staff
- Input validation and sanitization on backend

## Setup

1. Copy environment variables:

   ```bash
   cd backend
   copy .env.example .env
   ```

2. Install dependencies:

   ```bash
   npm run install-all
   ```

3. Start MongoDB locally or use a connection string in `backend/.env`.

4. Run the backend and frontend together from the repository root:

   ```bash
   npm run dev
   ```

   Alternatively, start each package separately:

   ```bash
   cd backend
   npm run dev
   ```

   ```bash
   cd frontend
   npm run dev
   ```

5. Open `http://localhost:3000` in your browser.

## Notes

- The frontend uses Vite and React Router.
- The backend proxies validation and provides secure auth logic.
- You can change JWT settings in `backend/.env`.

## Security reminders

- Never commit real secrets to source control.
- Use HTTPS in production.
- Store authentication tokens securely.
