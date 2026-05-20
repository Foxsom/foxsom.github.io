# Otago Exercise Program — Companion Web Application

A web-based companion portal built to support a smartphone application developed for the **Otago Exercise Program (OEP)**, a clinically validated fall-prevention exercise regimen for older adults. This project was created as part of a senior design capstone.

The site serves as the backend interface between clinicians and their patients, allowing clinicians to monitor patient progress and patients to log their exercise activity through the paired mobile app.

---

## Features

- **Role-based authentication** — Users are routed to separate dashboards based on their role (Clinician or Patient) upon login.
- **Firebase Authentication** — Secure email/password login with session persistence. Auth state is monitored in real time.
- **Firebase Realtime Database** — Patient and clinician data is read from and written to a Firebase database, enabling live data sync across devices.
- **Clinician portal** — Clinicians can view and manage their current clients.
- **Patient portal** — Patients are directed to their personal home page linked to their assigned clinician.
- **Account creation flows** — Separate registration pages for new users and new clinicians (`newUser.html`, `newClinician.html`).
- **CSV parsing** — PapaParse is integrated for any CSV-based data import/export.
- **Responsive design** — Mobile-friendly layout designed for use alongside a smartphone application.

---

## Tech Stack

| Technology | Purpose |
|---|---|
| HTML / CSS | Page structure and styling |
| JavaScript (Vanilla) | Application logic and Firebase integration |
| jQuery 3.3.1 | DOM manipulation and event handling |
| Firebase (v5.5.6) | Authentication and Realtime Database |
| Moment.js | Date/time formatting |
| PapaParse | CSV parsing |
| GitHub Pages | Hosting |

---

## Project Structure

```
/
├── index.html          # Login page — entry point for all users
├── functions.js        # Shared Firebase utility functions (init, DB refs, helpers)
├── newUser.html        # New patient registration page
├── newClinician.html   # New clinician registration page
├── physician/          # Clinician-facing views (client management)
└── user/               # Patient-facing views (exercise tracking home)
```

---

## How It Works

1. A user visits the site and is presented with a login modal.
2. Firebase Authentication verifies credentials and establishes a session.
3. The app checks the user's `isPhysician` flag in the Firebase Realtime Database.
4. Based on the role:
   - **Physicians** are redirected to `physician/currentClients.html`
   - **Patients** are redirected to `user/userHome.html`
5. New accounts can be created via the "New User" or "New Clinician" buttons on the login screen.

---

## Background

The **Otago Exercise Program** is a home-based strength and balance exercise program developed by the University of Otago (New Zealand) and shown in clinical trials to significantly reduce falls in older adults. This web portal was built as the clinician-facing companion to a mobile app that guides patients through the exercise program and tracks their progress.

This project was developed collaboratively as part of a senior design capstone course.

---

## Live Site

Hosted via GitHub Pages: [https://foxsom.github.io](https://foxsom.github.io)
