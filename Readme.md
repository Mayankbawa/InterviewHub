# InterviewHub– Automated Interview Scheduling System

## Project Overview

InterviewHub is a full-stack web application designed to automate the interview scheduling and management process. It intelligently matches candidates with interviewers based on skills, experience, and availability, reducing manual effort for HR teams and improving hiring efficiency.

The platform supports:
- Interviewer availability management
- Automatic candidate-interviewer assignment
- Interview feedback collection
- HR analytics dashboards

Built with React (frontend) and ASP.NET Core (backend), InterviewHubprovides a seamless and user-friendly experience for HR teams and interviewers.

## Features

1. Interviewer Management
   - Interviewers can define their available time slots.
   - Slots can be canceled with at least 3 hours notice.

2. Candidate Management
   - HR can register candidate profiles, including skills and years of experience.
   - Assign interviews automatically based on skill match.

3. Automatic Interview Scheduling
   - Background service assigns interviewers to candidates daily.
   - Matches are based on skills and experience.
   - Prevents double-booking or conflicts.

4. Interview Feedback
   - Interviewers can submit post-interview feedback.
   - Feedback includes technical skills, communication, and selection decision.
   - Data is visible in HR dashboards.

5. HR Dashboard
   - View total interviews, selected candidates, and rejection statistics.
   - Track interviewer participation and scheduling efficiency.

## Tech Stack

| Layer           | Technology                       |
|-----------------|---------------------------------|
| Frontend        | React, Vite, Axios, React Router|
| Backend         | ASP.NET Core Web API, C#        |
| Database        | SQL Server / Entity Framework   |
| Background Jobs | ASP.NET Core HostedService      |
| Charts          | Recharts / Chart.js             |

## Folder Structure

InterviewScheduler/
│
├── backend/
│   ├── InterviewScheduler.API/
│   │   ├── Controllers/
│   │   ├── Models/
│   │   ├── Data/
│   │   ├── Services/
│   │   ├── BackgroundJobs/
│   │   ├── Program.cs
│   │   └── appsettings.json
│
├── frontend/
│   ├── interview-scheduler-ui/
│   │   ├── public/
│   │   ├── src/
│   │   │   ├── components/
│   │   │   ├── pages/
│   │   │   ├── services/
│   │   │   ├── App.jsx
│   │   │   └── main.jsx
│   │   └── package.json
│
└── README.md

## How It Works

1. HR Registers Candidates & Interviewers
   - Candidate profiles with skills & experience
   - Interviewers with skills & available time slots

2. Automatic Assignment
   - Daily service checks candidates without interviews
   - Assigns interviewers based on skill match & availability

3. Interviewer Availability Management
   - Slots can be canceled at least 3 hours before scheduled interview

4. Interview Feedback
   - Interviewers submit post-interview evaluation
   - HR can view results in dashboards

5. HR Dashboard
   - Total interviews, selected candidates, rejected candidates
   - Metrics for interviewer participation and scheduling efficiency

## Installation & Setup

### Backend (ASP.NET Core)
cd backend/InterviewScheduler.API
dotnet restore
dotnet run

### Frontend (React)
cd frontend/interview-scheduler-ui
npm install
npm run dev

### Database
- Configure SQL Server connection in `appsettings.json`
- Run Entity Framework migrations to create tables:
dotnet ef database update

## Future Enhancements
- JWT Authentication with roles (HR / Interviewer)
- Email notifications for scheduled/canceled interviews
- AI-based skill matching recommendations
- Mobile-friendly interface

## Author
- Your Name  
- GitHub: [yourgithublink]  
- LinkedIn: [yourlinkedinlink]
