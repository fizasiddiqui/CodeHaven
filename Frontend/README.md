# Frontend - Interview Platform

A modern React-based frontend for an interview platform built with Vite, featuring real-time collaboration, code editing, and problem solving capabilities.

## Features

- Real-time collaborative coding interviews
- Monaco Editor integration for code editing
- Socket.io for real-time communication
- Responsive UI with Tailwind CSS
- Problem set management
- User authentication and profiles
- Submission tracking

## Tech Stack

- **React 18** - UI framework
- **Vite** - Build tool and dev server
- **React Router** - Client-side routing
- **Redux Toolkit** - State management
- **Socket.io Client** - Real-time communication
- **Monaco Editor** - Code editor
- **Tailwind CSS** - Styling
- **Axios** - HTTP client

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

1. Clone the repository
2. Navigate to the frontend directory:
   ```bash
   cd Frontend
   ```
3. Install dependencies:
   ```bash
   npm install
   ```

### Environment Variables

Create a `.env` file in the root of the frontend directory:

```env
VITE_BACKEND_URL=http://localhost:8000
```

### Development

Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:5173`

### Build for Production

```bash
npm run build
```

The built files will be in the `dist` directory.

## Deployment

### Render Deployment

1. Connect your GitHub repository to Render
2. Create a new Static Site service
3. Set the build command to: `npm run build`
4. Set the publish directory to: `dist`
5. Add environment variables in Render dashboard:
   - `VITE_BACKEND_URL` - Your backend service URL

### Vercel Deployment

1. Connect your GitHub repository to Vercel
2. Vercel will automatically detect the Vite configuration
3. Add environment variables in Vercel dashboard:
   - `VITE_BACKEND_URL` - Your backend service URL

## Project Structure

```
Frontend/
├── public/                 # Static assets
├── src/
│   ├── Components/         # React components
│   │   ├── Discuss/        # Discussion components
│   │   ├── Editor/         # Code editor components
│   │   ├── Header/         # Header component
│   │   ├── Home/           # Home page
│   │   ├── InterviewRooms/ # Interview room components
│   │   ├── Loading/        # Loading components
│   │   ├── Login/          # Authentication
│   │   ├── Problemset/     # Problem listing and details
│   │   ├── Profile/        # User profile
│   │   ├── Register/       # Registration
│   │   └── Submission/     # Submission tracking
│   ├── Features/           # Redux slices and store
│   ├── Services/           # API services
│   └── Store/              # Redux store configuration
├── .gitignore
├── eslint.config.js
├── index.html
├── package.json
├── postcss.config.js
├── README.md
├── render.yaml
├── tailwind.config.js
└── vite.config.js
```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run lint` - Run ESLint
- `npm run preview` - Preview production build locally

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests and linting
5. Submit a pull request

## License

This project is licensed under the ISC License.
