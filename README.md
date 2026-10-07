# Appointment Booking System

A full-stack appointment booking application built with React and Express.

## Project Structure

```
├── frontend/          # React frontend application
│   ├── src/
│   ├── public/
│   └── package.json
├── backend/           # Express backend API
│   ├── src/
│   └── package.json
└── README.md
```

## Features

- User authentication and authorization
- Appointment scheduling with calendar view
- Service provider management
- Admin dashboard
- Real-time availability checking
- Email notifications
- Appointment management (create, update, cancel)

## Tech Stack

### Frontend
- React 18
- TypeScript
- Vite
- React Router
- Axios
- Tailwind CSS
- React Calendar/Date Picker

### Backend
- Node.js
- Express
- TypeScript
- PostgreSQL
- Prisma ORM
- JWT Authentication
- Nodemailer

## Getting Started

### Prerequisites
- Node.js (v18 or higher)
- PostgreSQL
- npm or yarn

### Installation

1. Clone the repository
2. Install dependencies for both frontend and backend:

```bash
# Install backend dependencies
cd backend
npm install

# Install frontend dependencies
cd ../frontend
npm install
```

### Environment Setup

1. Backend (.env):
```env
DATABASE_URL="postgresql://user:password@localhost:5432/appointment_booking"
JWT_SECRET="your-secret-key"
PORT=5000
SMTP_HOST="your-smtp-host"
SMTP_PORT=587
SMTP_USER="your-email"
SMTP_PASS="your-password"
```

2. Frontend (.env):
```env
VITE_API_URL=http://localhost:5000/api
```

### Database Setup

```bash
cd backend
npx prisma migrate dev
npx prisma generate
```

### Running the Application

1. Start the backend:
```bash
cd backend
npm run dev
```

2. Start the frontend:
```bash
cd frontend
npm run dev
```

The frontend will be available at `http://localhost:5173` and the backend at `http://localhost:5000`.

## API Endpoints

### Authentication
- POST `/api/auth/register` - Register a new user
- POST `/api/auth/login` - Login user
- GET `/api/auth/me` - Get current user

### Appointments
- GET `/api/appointments` - Get all appointments
- GET `/api/appointments/:id` - Get appointment by ID
- POST `/api/appointments` - Create new appointment
- PUT `/api/appointments/:id` - Update appointment
- DELETE `/api/appointments/:id` - Cancel appointment

### Users
- GET `/api/users` - Get all users (admin)
- GET `/api/users/:id` - Get user by ID
- PUT `/api/users/:id` - Update user

### Services
- GET `/api/services` - Get all services
- POST `/api/services` - Create service (admin)
- PUT `/api/services/:id` - Update service (admin)
- DELETE `/api/services/:id` - Delete service (admin)

## License

MIT
