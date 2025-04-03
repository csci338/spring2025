---
title: "Full Stack Application: Student Academic Management Tool"
layout: assignment-two-column
type: project
draft: 0
points: 20
abbreviation: Project 2
num: 2
h_max: 5
start_date: 2025-04-03
due_date: 2025-05-05
---

<style>
    .info .highlight, .info .highlight pre, .info .highlight table {
        background: transparent !important;
        color: #242424 !important;
    }

    .info ol li, .info > ul > li {
        margin-bottom: 20px;
    }

    .info ol, .info > ul {
        margin-top: 20px !important;
    }

    .info code.highlighter-rouge {
        font-weight: bold;
        background: transparent;
    }

    .rubric td:first-child {
        min-width: 130px;
    }
</style>

{:.info}
> ## Team Preferences
> Please fill out the team preferences form <a href="https://forms.gle/xpSszwCG1uFDwvQe8" target="_blank">https://forms.gle/xpSszwCG1uFDwvQe8</a> by Friday, 4/4 at midnight.



## Objective
In this project, your team will design and build a web application that helps students manage their academic lives. The application must be built using:
- **React** for the frontend
- **FastAPI** for the backend
- **SQLAlchemy** for database interactions
- **PostgreSQL** as the database

Starter code will be provided, including the following:

### Backend Starter Code
- Prebuilt FastAPI endpoints:
  - `POST /api/token` – Get a JWT token.
  - `GET /api/courses` – Retrieves all available courses and filters on select attributes (e.g., instructor, location, etc.).
  - `GET /api/schedule/me/` – Retrieves courses associated with the logged-in user's schedule (basic functionality, in need of enhancements).
- User authentication system (JWT-based login/logout).
- Prebuilt PostgreSQL database with the following SQLAlchemy models:
  - User
  - Course
  - Instructor
  - Location
  - Schedule

### Frontend Starter Code
- Starter React app with:
  - Login screen
  - Simple search form to retrieve courses matching a user's query preferences
  - A fake schedule with some dummy classes

## Project Scope
Your team will extend this code to be more useful. The theme is **"student academic management"**, but you may interpret this broadly. Possible ideas include:

### Course Planner
- Enhancing the `/api/courses/` endpoint to allow searching by:
  - Course title (already implemented)
  - Instructor (already implemented)
  - Department
  - Time of day (morning, afternoon, evening)
  - Number of credit hours
  - Designation (e.g., First Year Seminar, Diversity Intensive, Honors, Service Learning)
  - Whether to show "open-only" classes
- Enhancing the schedule UI by displaying a weekly calendar of their courses.

### Study Group Manager
- Matches students with peers based on shared courses and availability.
- Could include a chat or note-taking feature.
- Each course could have an area for taking notes, uploading screenshots, etc.

### Internship / REU Tracker
- Assists students in tracking job applications and networking contacts.
- Helps plan how to incorporate course assignments/projects into a resume, LinkedIn, GitHub, or portfolio.

### Task / Assignment Tracker
- Users log assignments, deadlines, and progress for each course.
- Could include email/text notifications.

### Work/Life Balance Support
- Helps students consider how coursework supports other life priorities.

### Some other idea of your choice...
- Feel free to propose your own interpretation of this assignment. Creativity is encouraged.

## Minimum Required Features
All teams must:
- Create at least **two new database models** (e.g., `StudySession`, `Internship`, `StudyGroup`, `Task`).
- Build FastAPI endpoints for any relevant **CRUD operations** (Create, Read, Update, Delete) needed to suppor the functionality of your site.
- Develop React UI components/screens to interact with FastAPI endpoints.
- Give the app a **look and feel** (colors, fonts, styling, accessibility, usability, etc.).
- **Enforce security** (users should not see data that doesn’t belong to them).
- Write **tests** for all backend functionality (you don't need to run tessts for React stuff) and ensure linter/formatter checks pass.

## Optional Stretch Goals (Extra Credit)
Each feature below is worth **5 points** (maximum of **10 extra points**):

- **Calendar API integration** (sync with Google Calendar).
- **Collaboration/chat features** – Share schedules, chat with other logged-in users.
- **Email or text notifications** for schedule updates or reminders.
- **Cloud deployment** – Update Dockerfile to integrate dependencies and schemas.
- **Automated course data updates** – Periodically refresh course listings from the Meteor site.
- **Waitlist feature** – Display real-time seat availability and send notifications when a course opens.
- **Admin dashboard**:
  - Allow instructors/admins to modify course offerings.
  - Provide analytics on course popularity.
- **UI Enhancements**:
  - Add dark mode.
  - Improve keyboard navigation and screen reader compatibility.
  - Ensure full responsiveness and mobile-friendliness.
- **Propose your own stretch goal!**

## Deliverables

{:.rubric}
| Week  | Milestone |
|-------|-----------|
| **Week 1 (4/11)** | Set up repo, install Docker dependencies, run the app locally, familiarize with code, submit project description (1-page plan, basic wireframe, API endpoint descriptions). |
| **Week 3 (4/25)** | Midpoint Deliverable: Working modifications to backend and frontend. |
| **Week 5 (5/6)** | Final Submission – Complete project, presentation, and final GitHub push. |

## Grading Criteria (100 Points)

| Category | Points | Description |
|----------|--------|-------------|
| **Project Proposal** | 5 | 1-page plan, basic wireframe, API endpoint descriptions. |
| **Midpoint Deliverable** | 10 | At least 1 meanful feature is implemented per teammate. |
| **Backend Functionality** | 35 | API and database work correctly (CRUD operations) + Tests. |
| **Frontend Functionality** | 20 | React app interacts successfully with the API. |
| **UI/UX Design** | 10 | Simple but intuitive frontend. |
| **Code Quality** | 15 | Clean, modular, readable code with meaningful commits. |
| **Final Presentation** | 5 | 5-minute demo with a clear feature explanation. |
