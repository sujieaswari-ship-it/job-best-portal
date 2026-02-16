# Job Portal

A modern job portal application with React frontend, Node.js backend, and MongoDB database.

## Features

- Job posting and search
- User authentication (job seekers and employers)
- Application management
- Responsive design with modern UI
- Real-time notifications

## Tech Stack

### Frontend
- React 18
- TypeScript
- TailwindCSS
- shadcn/ui
- React Query
- React Router

### Backend
- Node.js
- Express
- TypeScript
- MongoDB
- JWT Authentication
- bcrypt

### Database
- MongoDB with Mongoose ODM

## Getting Started

### Prerequisites
- Node.js 18+
- MongoDB
- npm or yarn

### Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   # Frontend
   cd frontend
   npm install
   
   # Backend
   cd backend
   npm install
   ```

3. Set up environment variables (see .env.example)
4. Start the development servers:
   ```bash
   # Backend
   cd backend
   npm run dev
   
   # Frontend
   cd frontend
   npm start
   ```

## Project Structure

```
job-portal/
├── frontend/          # React frontend
├── backend/           # Node.js backend
├── shared/            # Shared types and utilities
└── README.md
```
