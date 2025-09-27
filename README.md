<<<<<<< HEAD
# EduGameHub Backend API

A comprehensive Node.js/Express backend for the EduGameHub gamified educational platform. This backend provides RESTful APIs for user authentication, event management, achievement tracking, and student progress monitoring.

## 🎯 Project Overview

This backend serves as the API layer for EduGameHub, a gamified educational platform where students can track their academic, sports, and extracurricular progress while earning points and achievements.
=======
# EduGameHub Frontend

A modern React frontend for the EduGameHub gamified educational platform. This frontend provides an intuitive user interface for students and administrators to interact with the backend API.

## 🎯 Project Overview

This React application serves as the user interface for EduGameHub, allowing students to track their progress, participate in events, earn achievements, and compete on leaderboards. Administrators can manage events, award points, and monitor student progress.
>>>>>>> eeb1517 (first commit)

## 🚀 Quick Start

### Prerequisites
- **Node.js** (v16 or higher) - [Download here](https://nodejs.org/)
<<<<<<< HEAD
- **MongoDB** (local or Atlas account) - [Download here](https://www.mongodb.com/try/download/community) or [Atlas here](https://www.mongodb.com/atlas)
=======
- **EduGameHub Backend** running on http://localhost:5000
>>>>>>> eeb1517 (first commit)
- **Git** - [Download here](https://git-scm.com/)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
<<<<<<< HEAD
   cd edugamehub-backend
=======
   cd edugamehub-frontend
>>>>>>> eeb1517 (first commit)
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
<<<<<<< HEAD
   ```bash
   cp env.example .env
   ```

4. **Configure Environment Variables**
   Edit `.env` file:
   ```env
   # Server Configuration
   PORT=5000
   NODE_ENV=development

   # Database Configuration
   MONGODB_URI=mongodb://localhost:27017/edugamehub
   # OR for MongoDB Atlas:
   # MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/edugamehub

   # JWT Configuration
   JWT_SECRET=your_super_secret_jwt_key_change_this_in_production
   JWT_EXPIRE=7d

   # CORS Configuration
   FRONTEND_URL=http://localhost:5173

   # Rate Limiting
   RATE_LIMIT_WINDOW_MS=900000
   RATE_LIMIT_MAX_REQUESTS=100
   ```

5. **Start MongoDB**
   ```bash
   # Local MongoDB
   brew services start mongodb-community  # macOS
   # OR use MongoDB Atlas (cloud)
   ```

6. **Seed Database (Optional)**
   ```bash
   npm run seed
   ```

7. **Start Development Server**
=======
   Create `.env` file in the root directory:
   ```env
   VITE_API_URL=http://localhost:5000/api
   ```

4. **Start Development Server**
>>>>>>> eeb1517 (first commit)
   ```bash
   npm run dev
   ```

<<<<<<< HEAD
## 📁 Project Structure

```
edugamehub-backend/
├── config/                 # Configuration files
├── controllers/           # Route controllers
│   ├── authController.js
│   ├── userController.js
│   ├── eventController.js
│   └── achievementController.js
├── middleware/            # Custom middleware
│   ├── auth.js
│   └── errorHandler.js
├── models/               # Mongoose models
│   ├── User.js
│   ├── Event.js
│   └── Achievement.js
├── routes/               # API routes
│   ├── auth.js
│   ├── users.js
│   ├── events.js
│   └── achievements.js
├── scripts/              # Database scripts
│   └── seedDatabase.js
├── utils/                # Utility functions
├── server.js             # Main server file
├── package.json          # Dependencies
├── env.example           # Environment template
└── README.md             # This file
=======
5. **Access the Application**
   Open [http://localhost:5173](http://localhost:5173) in your browser

## 📁 Project Structure

```
edugamehub-frontend/
├── src/
│   ├── components/        # Reusable components
│   │   ├── ui/           # shadcn/ui components
│   │   ├── AchievementBadge.tsx
│   │   ├── ProgressCard.tsx
│   │   ├── ThemeProvider.tsx
│   │   └── ThemeToggle.tsx
│   ├── contexts/          # React contexts
│   │   └── AuthContext.tsx
│   ├── hooks/             # Custom hooks
│   │   ├── use-mobile.tsx
│   │   └── use-toast.ts
│   ├── pages/             # Page components
│   │   ├── Index.tsx
│   │   ├── LoginSelection.tsx
│   │   ├── StudentLogin.tsx
│   │   ├── AdminLogin.tsx
│   │   ├── StudentDashboard.tsx
│   │   ├── AdminDashboard.tsx
│   │   └── NotFound.tsx
│   ├── services/          # API services
│   │   └── api.ts
│   ├── lib/               # Utility functions
│   │   └── utils.ts
│   ├── App.tsx            # Main app component
│   └── main.tsx           # Frontend entry point
├── public/                # Static assets
├── package.json           # Dependencies
├── vite.config.ts         # Vite configuration
├── tailwind.config.ts     # Tailwind CSS configuration
├── tsconfig.json          # TypeScript configuration
└── README.md              # This file
>>>>>>> eeb1517 (first commit)
```

## 🛠️ Available Scripts

```bash
# Development
<<<<<<< HEAD
npm run dev          # Start development server with nodemon
npm start            # Start production server

# Database
npm run seed         # Seed database with demo data

# Testing
npm test             # Run tests
npm run test:watch   # Run tests in watch mode
```

## 📚 API Documentation

### Base URL
```
http://localhost:5000/api
```

### Authentication Endpoints

| Method | Endpoint | Description | Access |
|--------|----------|-------------|--------|
| POST | `/auth/register` | Register new user | Public |
| POST | `/auth/login` | Login user | Public |
| GET | `/auth/me` | Get current user | Private |
| PUT | `/auth/updatedetails` | Update user details | Private |
| PUT | `/auth/updatepassword` | Update password | Private |
| POST | `/auth/logout` | Logout user | Private |

### User Endpoints

| Method | Endpoint | Description | Access |
|--------|----------|-------------|--------|
| GET | `/users` | Get all users | Admin |
| GET | `/users/leaderboard` | Get leaderboard | Private |
| GET | `/users/profile/:id` | Get user profile | Private |
| PUT | `/users/:id` | Update user | Admin |
| DELETE | `/users/:id` | Delete user | Admin |
| GET | `/users/stats` | Get user statistics | Admin |

### Event Endpoints

| Method | Endpoint | Description | Access |
|--------|----------|-------------|--------|
| GET | `/events` | Get all events | Private |
| GET | `/events/upcoming` | Get upcoming events | Private |
| GET | `/events/department/:dept` | Get events by department | Private |
| GET | `/events/:id` | Get single event | Private |
| POST | `/events` | Create event | Admin |
| PUT | `/events/:id` | Update event | Admin |
| DELETE | `/events/:id` | Delete event | Admin |
| POST | `/events/:id/participate` | Participate in event | Private |
| DELETE | `/events/:id/participate` | Remove participation | Private |

### Achievement Endpoints

| Method | Endpoint | Description | Access |
|--------|----------|-------------|--------|
| GET | `/achievements` | Get all achievements | Private |
| GET | `/achievements/category/:category` | Get achievements by category | Private |
| GET | `/achievements/rare` | Get rare achievements | Private |
| GET | `/achievements/user/:userId` | Get user achievements | Private |
| GET | `/achievements/:id` | Get single achievement | Private |
| POST | `/achievements` | Create achievement | Admin |
| PUT | `/achievements/:id` | Update achievement | Admin |
| DELETE | `/achievements/:id` | Delete achievement | Admin |
| POST | `/achievements/check` | Check user achievements | Private |

## 🔐 Authentication

The API uses JWT (JSON Web Tokens) for authentication. Include the token in the Authorization header:

```
Authorization: Bearer <your-jwt-token>
```

## 📝 Example Requests

### Register a Student
```bash
curl -X POST http://localhost:5000/api/auth/register \
  -H "Content-Type: application/json" \
  -d '{
    "name": "John Doe",
    "email": "john@demo.edu",
    "password": "password123",
    "role": "student",
    "studentId": "CS2021001",
    "department": "Computer Science",
    "year": "3rd Year"
  }'
```

### Login
```bash
curl -X POST http://localhost:5000/api/auth/login \
  -H "Content-Type: application/json" \
  -d '{
    "email": "student@demo.edu",
    "password": "demo123"
  }'
```

### Create Event (Admin)
```bash
curl -X POST http://localhost:5000/api/events \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <admin-token>" \
  -d '{
    "title": "Mid-Semester Exam",
    "description": "Comprehensive exam covering all topics",
    "type": "academic",
    "points": 200,
    "department": "Computer Science",
    "date": "2024-04-15"
  }'
```

## 🗄️ Database Models

### User Model
```javascript
{
  name: String,
  email: String (unique),
  password: String (hashed),
  role: String (student/admin),
  studentId: String (unique),
  department: String,
  year: String,
  totalPoints: Number,
  level: Number,
  achievements: [ObjectId],
  eventsParticipated: [ObjectId],
  isActive: Boolean,
  lastLogin: Date,
  createdAt: Date,
  updatedAt: Date
}
```

### Event Model
```javascript
{
  title: String,
  description: String,
  type: String (academic/sports/extracurricular),
  points: Number,
  department: String,
  date: Date,
  status: String (upcoming/ongoing/completed/cancelled),
  participants: [ObjectId],
  maxParticipants: Number,
  createdBy: ObjectId,
  isActive: Boolean,
  createdAt: Date,
  updatedAt: Date
}
```

### Achievement Model
```javascript
{
  title: String,
  description: String,
  category: String (academic/sports/extracurricular/special),
  rarity: String (common/rare/epic/legendary),
  points: Number,
  requirements: {
    type: String (points/events/streak/custom),
    value: Number,
    description: String
  },
  icon: String,
  createdBy: ObjectId,
  isActive: Boolean,
  createdAt: Date,
  updatedAt: Date
}
```
=======
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build

# Code Quality
npm run lint         # Run ESLint
```

## 🎨 UI Components

This project uses **shadcn/ui** components built on top of:
- **Radix UI** - Accessible component primitives
- **Tailwind CSS** - Utility-first CSS framework
- **Lucide React** - Beautiful icons

### Key Components
- **Authentication Forms** - Login and registration
- **Dashboard Layouts** - Student and admin dashboards
- **Progress Cards** - Visual progress tracking
- **Achievement Badges** - Gamified achievements
- **Data Tables** - Event and user management
- **Charts** - Progress visualization

## 🔐 Authentication Flow

### Student Authentication
1. **Login Selection** - Choose student or admin portal
2. **Student Login** - Email/password authentication
3. **Dashboard Access** - Personalized student dashboard
4. **Progress Tracking** - View points, level, and achievements

### Admin Authentication
1. **Admin Login** - Admin credentials
2. **Admin Dashboard** - Management interface
3. **Event Management** - Create and manage events
4. **User Management** - Monitor student progress

## 📊 Features

### Student Features
- **Progress Tracking** - Academic, sports, and extracurricular progress
- **Achievement System** - Unlock achievements with different rarity levels
- **Event Participation** - Join events and earn points
- **Leaderboards** - Department and college rankings
- **Profile Management** - Update personal information

### Admin Features
- **Event Management** - Create, update, and delete events
- **Achievement Management** - Create and manage achievements
- **User Management** - View and manage student accounts
- **Analytics** - Student progress and engagement metrics
- **Point System** - Award points for various activities

## 🔌 API Integration

The frontend communicates with the backend through a centralized API service:

### API Service Features
- **Centralized Configuration** - Single point for API URL configuration
- **Token Management** - Automatic JWT token handling
- **Error Handling** - Consistent error handling across the app
- **Request/Response Interceptors** - Automatic token attachment and error processing

### Authentication Context
- **State Management** - Centralized authentication state
- **User Data** - Current user information and permissions
- **Login/Logout** - Authentication flow management
- **Token Persistence** - Automatic token storage and retrieval

## 🎯 Key Technologies

- **React 18** - Modern React with hooks
- **TypeScript** - Type-safe JavaScript
- **Vite** - Fast build tool and dev server
- **Tailwind CSS** - Utility-first CSS framework
- **shadcn/ui** - High-quality component library
- **React Router** - Client-side routing
- **Context API** - State management
- **Axios** - HTTP client for API calls

## 🧪 Testing

### Manual Testing
1. **Start Backend** - Ensure EduGameHub backend is running
2. **Start Frontend** - Run `npm run dev`
3. **Test Authentication** - Try login with demo credentials
4. **Test Features** - Navigate through all application features

### Demo Credentials
- **Student**: student@demo.edu / demo123
- **Admin**: admin@demo.edu / admin123

## 🚀 Deployment

### Build for Production
```bash
npm run build
```

### Deploy to Vercel
1. Connect GitHub repository to Vercel
2. Set build command: `npm run build`
3. Set output directory: `dist`
4. Add environment variable: `VITE_API_URL=https://your-backend-url.com/api`

### Deploy to Netlify
1. Connect GitHub repository to Netlify
2. Set build command: `npm run build`
3. Set publish directory: `dist`
4. Add environment variable: `VITE_API_URL=https://your-backend-url.com/api`
>>>>>>> eeb1517 (first commit)

## 🔧 Development

### Adding New Features

<<<<<<< HEAD
1. **Create Model** (if needed)
   ```bash
   # Add new model in models/
   ```

2. **Create Controller**
   ```bash
   # Add controller logic in controllers/
   ```

3. **Create Routes**
   ```bash
   # Add routes in routes/
   ```

4. **Update Server**
   ```bash
   # Import and use routes in server.js
=======
1. **Create Components**
   ```bash
   # Add new components in src/components/
   ```

2. **Create Pages**
   ```bash
   # Add new pages in src/pages/
   ```

3. **Update API Service**
   ```bash
   # Add new API methods in src/services/api.ts
   ```

4. **Update Routes**
   ```bash
   # Add new routes in src/App.tsx
>>>>>>> eeb1517 (first commit)
   ```

### Code Style

<<<<<<< HEAD
- Use async/await for asynchronous operations
- Implement proper error handling
- Add input validation
- Follow RESTful API conventions
- Use meaningful variable names
- Add comments for complex logic

## 🧪 Testing

### Manual Testing with Postman
1. Import the Postman collection
2. Set up environment variables
3. Test all endpoints

### Automated Testing
```bash
npm test
```

## 🚀 Deployment

### Environment Variables for Production
```env
NODE_ENV=production
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/edugamehub
JWT_SECRET=your_production_jwt_secret
FRONTEND_URL=https://your-frontend-domain.com
```

### Deployment Platforms
- **Railway**: Easy deployment with GitHub integration
- **Heroku**: Popular platform with good documentation
- **DigitalOcean**: VPS with full control
- **AWS**: Enterprise-grade cloud platform

## 🔑 Demo Credentials

After running `npm run seed`:

### Admin Account
- **Email**: admin@demo.edu
- **Password**: admin123
- **Role**: Admin

### Student Account
- **Email**: student@demo.edu
- **Password**: demo123
- **Role**: Student
- **Department**: Computer Science
- **Points**: 2850
- **Level**: 12

## 🛠️ Key Technologies Used

- **Node.js**: JavaScript runtime
- **Express.js**: Web framework
- **MongoDB**: NoSQL database
- **Mongoose**: MongoDB object modeling
- **JWT**: JSON Web Tokens for authentication
- **bcryptjs**: Password hashing
- **express-validator**: Input validation
- **helmet**: Security middleware
- **cors**: Cross-origin resource sharing
- **morgan**: HTTP request logger

## 📚 Learning Objectives

By working with this backend, you'll learn:

1. **Node.js Fundamentals**
   - Module system and package management
   - Asynchronous programming with async/await
   - File system operations

2. **Express.js**
   - Middleware architecture
   - Route handling and parameters
   - Request/response cycle
   - Error handling

3. **MongoDB with Mongoose**
   - Schema design and validation
   - CRUD operations
   - Relationships and population
   - Indexing for performance

4. **Authentication & Security**
   - JWT implementation
   - Password hashing
   - Role-based access control
   - Input validation and sanitization

5. **API Design**
   - RESTful principles
   - HTTP methods and status codes
   - Request/response formatting
   - Error handling patterns

6. **Production Considerations**
   - Environment configuration
   - Security best practices
   - Performance optimization
   - Deployment strategies
=======
- Use TypeScript for type safety
- Follow React hooks patterns
- Use Tailwind CSS for styling
- Implement proper error handling
- Add loading states for async operations

## 📚 Learning Objectives

By working with this frontend, you'll learn:

1. **React Fundamentals**
   - Component architecture
   - Hooks and state management
   - Event handling and forms
   - Conditional rendering

2. **TypeScript**
   - Type definitions
   - Interface design
   - Type safety
   - Generic types

3. **Modern CSS**
   - Tailwind CSS utilities
   - Responsive design
   - Component styling
   - Dark mode support

4. **State Management**
   - Context API
   - Custom hooks
   - State persistence
   - Error boundaries

5. **API Integration**
   - HTTP requests
   - Authentication handling
   - Error management
   - Loading states

6. **Build Tools**
   - Vite configuration
   - TypeScript compilation
   - CSS processing
   - Asset optimization
>>>>>>> eeb1517 (first commit)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License.

## 🆘 Support

For questions or issues:
- Check the troubleshooting section
<<<<<<< HEAD
- Review error logs
- Ask questions during workshop sessions
- Use online documentation and Stack Overflow

## 🎉 Next Steps

1. **Explore the codebase** - Understand the project structure
2. **Run the application** - Test all endpoints
3. **Modify and extend** - Add new features
4. **Deploy to production** - Learn deployment strategies
5. **Integrate with frontend** - Connect with React application

This backend provides a solid foundation for building modern web applications with the MERN stack!"# mce-student-portal-frontend" 
=======
- Review browser console for errors
- Ensure backend is running
- Check network requests in DevTools

## 🎉 Next Steps

1. **Explore the codebase** - Understand the component structure
2. **Run the application** - Test all features
3. **Modify components** - Customize the UI
4. **Add new features** - Extend functionality
5. **Deploy to production** - Share your application

This frontend provides a solid foundation for building modern React applications with TypeScript and Tailwind CSS!
"# mce-student-portal-frontend" 
>>>>>>> eeb1517 (first commit)
