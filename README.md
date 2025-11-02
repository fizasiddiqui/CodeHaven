# CodeHaven

CodeHaven is a comprehensive coding interview platform that allows users to practice coding problems, participate in real-time mock interviews, and collaborate on solutions. It features a React-based frontend for an intuitive user interface and a Node.js/Express backend with Socket.io for real-time communication.

## Features

- **Problem Solving**: Access a curated set of coding problems with sample cases and execution environments.
- **Real-Time Interviews**: Host and join mock interviews with live code sharing, video calls, and collaborative editing.
- **User Authentication**: Secure login and registration system.
- **Code Execution**: Run and test code submissions in multiple languages.
- **Discussion Forums**: Engage in problem discussions and share solutions.
- **Profile Management**: Track problem-solving stats and manage user profiles.

## Tech Stack

### Frontend
- React (Vite)
- Tailwind CSS
- Axios for API calls
- Socket.io client for real-time features

### Backend
- Node.js
- Express.js
- MongoDB (Mongoose)
- Socket.io for real-time communication
- JWT for authentication
- Cloudinary for image uploads

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn
- MongoDB (local or cloud instance like MongoDB Atlas)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/fizasiddiqui/CodeHaven.git
   cd CodeHaven
   ```

2. Set up the backend:
   ```bash
   cd Backend
   npm install
   cp .env.example .env  # Configure your environment variables
   npm run dev
   ```

3. Set up the frontend (in a new terminal):
   ```bash
   cd Frontend
   npm install
   npm run dev
   ```

4. Open your browser and navigate to `http://localhost:5173` for the frontend. The backend runs on `http://localhost:8000`.

### Environment Variables

Create a `.env` file in the Backend directory with the following variables:
- `MONGODB_URI`: Your MongoDB connection string
- `CORS_ORIGIN`: Frontend URL (e.g., `http://localhost:5173` for development)
- `JWT_SECRET`: Secret key for JWT tokens
- `CLOUDINARY_CLOUD_NAME`, `CLOUDINARY_API_KEY`, `CLOUDINARY_API_SECRET`: For image uploads

## Deployment

This project is configured for deployment on Render. See the detailed deployment instructions in the respective subfolder READMEs:

- [Backend Deployment](./Backend/README.md)
- [Frontend Deployment](./Frontend/README.md)

## Project Structure

```
CodeHaven/
├── Backend/          # Node.js/Express API server
│   ├── src/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── middlewares/
│   │   ├── utils/
│   │   └── SocketIo/
│   ├── package.json
│   └── README.md
├── Frontend/         # React/Vite client application
│   ├── src/
│   │   ├── Components/
│   │   ├── Features/
│   │   ├── Services/
│   │   └── Store/
│   ├── package.json
│   └── README.md
└── README.md         # This file
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

## Support

If you have any questions or issues, please open an issue on GitHub or contact the maintainers.
