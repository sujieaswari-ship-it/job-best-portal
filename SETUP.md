# Job Portal Setup Instructions

## Prerequisites
- Node.js 18+ installed
- MongoDB installed and running
- Git (optional)

## Quick Start

### 1. Install Dependencies

**Backend:**
```bash
cd backend
npm install
```

**Frontend:**
```bash
cd frontend
npm install
```

### 2. Environment Setup

**Backend:**
Copy `backend/.env.example` to `backend/.env` and update:
- `MONGODB_URI`: Your MongoDB connection string
- `JWT_SECRET`: A secure secret key
- `FRONTEND_URL`: Frontend URL (default: http://localhost:3000)

### 3. Start the Application

**Option 1: Use the batch file (Windows)**
```bash
start.bat
```

**Option 2: Manual startup**

Terminal 1 - Backend:
```bash
cd backend
npm run dev
```

Terminal 2 - Frontend:
```bash
cd frontend
npm start
```

### 4. Access the Application

- Frontend: http://localhost:3000
- Backend API: http://localhost:5000
- API Health Check: http://localhost:5000/api/health

## Features Available

### User Authentication
- Registration (Job Seeker/Employer)
- Login with JWT tokens
- Profile management

### Job Management
- Post new jobs (Employers only)
- Search and filter jobs
- View job details
- Update/delete own jobs

### Application System
- Apply for jobs (Job Seekers)
- Track application status
- Manage applications (Employers)

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login
- `GET /api/auth/profile` - Get user profile

### Jobs
- `GET /api/jobs` - Get all jobs with filters
- `GET /api/jobs/search` - Search jobs
- `GET /api/jobs/:id` - Get job by ID
- `POST /api/jobs` - Create new job (Employer)
- `PUT /api/jobs/:id` - Update job (Employer)
- `DELETE /api/jobs/:id` - Delete job (Employer)

### Applications
- `POST /api/applications` - Submit application (Job Seeker)
- `GET /api/applications` - Get all applications (Employer)
- `GET /api/applications/my-applications` - Get user applications (Job Seeker)
- `PUT /api/applications/:id/status` - Update application status (Employer)

## Troubleshooting

### Backend Issues
- Ensure MongoDB is running
- Check environment variables in `.env`
- Verify port 5000 is not in use

### Frontend Issues
- Clear browser cache
- Check if backend is running on port 5000
- Verify proxy configuration in package.json

### Common Issues
1. **MongoDB Connection**: Make sure MongoDB service is running
2. **Port Conflicts**: Change ports in `.env` if needed
3. **CORS Issues**: Verify FRONTEND_URL in backend `.env`
4. **TypeScript Errors**: Run `npm run build` to check for issues

## Development Notes

- Backend runs on port 5000
- Frontend runs on port 3000
- Hot reload enabled for both
- API documentation available at `/api/health` endpoint
