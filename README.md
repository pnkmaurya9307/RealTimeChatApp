# LotusChat 💬

A real-time chat application built with the MERN stack and Socket.IO. Sign up, find other users, chat with them instantly, share images, and see who's online — all in real time.

## Features

- 🔐 Secure authentication with JWT (stored in HTTP-only cookies) and hashed passwords
- ⚡ Real-time one-to-one messaging powered by Socket.IO
- 🟢 Online/offline status indicators
- 🖼️ Image sharing in chat, uploaded and served via Cloudinary
- 🔎 Search for other users by name/username
- 👤 Editable user profile with profile picture upload
- 😀 Emoji picker for messages
- 📱 Responsive UI built with Tailwind CSS

## Tech Stack

**Frontend**
- React 19 + Vite
- Redux Toolkit (state management)
- React Router
- Tailwind CSS
- Axios
- Socket.IO Client

**Backend**
- Node.js + Express 5
- MongoDB + Mongoose
- Socket.IO
- JSON Web Tokens (JWT) for auth
- bcryptjs for password hashing
- Multer + Cloudinary for image uploads

## Project Structure

```
LotusChat/
├── backend/
│   ├── config/          # DB, Cloudinary, and token config
│   ├── controllers/     # Route handlers (auth, user, message)
│   ├── middlewares/     # Auth guard, Multer file upload
│   ├── models/          # Mongoose schemas (User, Message, Conversation)
│   ├── routes/          # Express route definitions
│   ├── socket/          # Socket.IO server setup
│   └── index.js         # App entry point
└── frontend/
    ├── src/
    │   ├── components/  # Sidebar, Message area, Message bubbles
    │   ├── customHooks/ # Hooks for fetching users, messages, current user
    │   ├── pages/        # Login, SignUp, Home, Profile
    │   └── redux/        # Redux slices (user, message)
    └── index.html
```

## Prerequisites

- [Node.js](https://nodejs.org/) v18 or higher
- A free [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) cluster (or a local MongoDB instance)
- A free [Cloudinary](https://cloudinary.com/) account (for image uploads)

## Setup

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd LotusChat
```

### 2. Backend setup

```bash
cd backend
npm install
```

Create a `.env` file inside the `backend` folder with the following variables:

```env
PORT=8000
MONGODB_URL="your-mongodb-connection-string"
JWT_SECRET="your-random-secret-string"
CLOUD_NAME="your-cloudinary-cloud-name"
API_KEY="your-cloudinary-api-key"
API_SECRET="your-cloudinary-api-secret"
```

Start the backend server:

```bash
npm run dev
```

The server will run on `http://localhost:8000`.

### 3. Frontend setup

Open a new terminal:

```bash
cd frontend
npm install
npm run dev
```

The app will be available at `http://localhost:5173`.

## Usage

1. Open `http://localhost:5173` in your browser and create an account.
2. Search for or select another registered user from the sidebar.
3. Start chatting in real time — send text messages and images.
4. Use a separate browser, incognito window, or browser profile to log in as a second user and test real-time messaging between two accounts.

## Environment Variables Reference

| Variable | Description |
|---|---|
| `PORT` | Port the backend server runs on (default: `8000`) |
| `MONGODB_URL` | MongoDB connection string |
| `JWT_SECRET` | Secret key used to sign JWT auth tokens |
| `CLOUD_NAME` | Cloudinary cloud name |
| `API_KEY` | Cloudinary API key |
| `API_SECRET` | Cloudinary API secret |

## License

This project is for personal/educational use.