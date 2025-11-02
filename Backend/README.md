# Backend - Interview Platform API

A Node.js/Express backend API for an interview platform with real-time collaboration features using Socket.io.

## Features

- User authentication and authorization (JWT)
- Problem management and code execution
- Real-time interview rooms with Socket.io
- File upload handling with Cloudinary
- Tweet/discussion system
- Submission tracking and results
- MongoDB database integration

## Tech Stack

- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **Socket.io** - Real-time communication
- **JWT** - Authentication
- **Bcrypt** - Password hashing
- **Cloudinary** - File storage
- **Multer** - File upload handling

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- MongoDB (local or cloud instance)
- npm or yarn

### Installation

1. Clone the repository
2. Navigate to the backend directory:
   ```bash
   cd Backend
   ```
3. Install dependencies:
   ```bash
   npm install
   ```

### Environment Variables

Create a `.env` file in the root of the backend directory:

```env
# Database
MONGODB_URI=mongodb://localhost:27017/interview-platform

# JWT
ACCESS_TOKEN_SECRET=your_access_token_secret
ACCESS_TOKEN_EXPIRY=1d
REFRESH_TOKEN_SECRET=your_refresh_token_secret
REFRESH_TOKEN_EXPIRY=10d

# Cloudinary (for file uploads)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# CORS Origin
CORS_ORIGIN=http://localhost:5173

# Port
PORT=8000
```

### Development

Start the development server:
```bash
npm run dev
```

The server will start on port 8000 (or the port specified in your `.env` file).

### Production

Build and start for production:
```bash
npm start
```

## API Endpoints

### Authentication
- `POST /api/v1/users/register` - User registration
- `POST /api/v1/users/login` - User login
- `POST /api/v1/users/logout` - User logout
- `POST /api/v1/users/refresh-token` - Refresh access token

### Users
- `GET /api/v1/users/current-user` - Get current user
- `PATCH /api/v1/users/update-account` - Update account details
- `PATCH /api/v1/users/update-avatar` - Update avatar
- `PATCH /api/v1/users/change-password` - Change password

### Problems
- `GET /api/v1/problem/all` - Get all problems
- `GET /api/v1/problem/:id` - Get problem by ID
- `POST /api/v1/problem/create` - Create new problem (admin)
- `PATCH /api/v1/problem/:id` - Update problem (admin)
- `DELETE /api/v1/problem/:id` - Delete problem (admin)

### Code Execution
- `POST /api/v1/runcode/run` - Execute code

### Submissions
- `GET /api/v1/submissions/user/:userId` - Get user submissions
- `POST /api/v1/submissions/submit` - Submit solution

### Tweets/Discussions
- `GET /api/v1/tweet/all` - Get all tweets
- `POST /api/v1/tweet/create` - Create tweet
- `DELETE /api/v1/tweet/:id` - Delete tweet

## Socket.io Events

### Interview Rooms
- `create-room` - Create new interview room
- `room:join_request` - Request to join room
- `host:req_accepted` - Host accepts join request
- `host:leave` - Host leaves room
- `interviewee:leave` - Interviewee leaves room

### Code Collaboration
- `code:change` - Code changes in editor
- `question:change` - Question/problem changes
- `language:change` - Programming language changes
- `cases:change` - Test cases changes
- `code:run` - Run code execution
- `time:change` - Timer changes

### Video Calling
- `user:call` - Initiate video call
- `call:accepted` - Accept video call
- `set:share_streams` - Set up stream sharing
- `peer:nego:needed` - Peer negotiation needed
- `peer:nego:done` - Peer negotiation done

## Project Structure

```
Backend/
├── src/
│   ├── controllers/        # Route controllers
│   ├── db/                 # Database connection
│   ├── middlewares/        # Express middlewares
│   ├── models/             # Mongoose models
│   ├── routes/             # API routes
│   ├── SocketIo/           # Socket.io configuration
│   ├── utils/              # Utility functions
│   ├── app.js              # Express app setup
│   ├── constants.js        # App constants
│   └── server.js           # Server entry point
├── public/                 # Static files
├── .env                    # Environment variables
├── .gitignore
├── package.json
├── README.md
├── render.yaml             # Render deployment config
└── vercel.json             # Vercel deployment config
```

## Deployment

### Render Deployment

1. Connect your GitHub repository to Render
2. Create a new Web Service
3. Set the runtime to Node.js
4. Set the build command to: `npm install`
5. Set the start command to: `npm start`
6. Add environment variables in Render dashboard
7. Deploy

### Manual Deployment

1. Set up a server with Node.js installed
2. Clone the repository
3. Install dependencies: `npm install`
4. Set up environment variables
5. Start the server: `npm start`

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the ISC License.
