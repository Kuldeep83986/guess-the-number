# Guess the Number Game
A full-stack web application where users can register, log in, and play a fun "Guess the Number" game while tracking their score on a global leaderboard.

<img width="1898" height="867" alt="Screenshot 2026-03-25 140445" src="https://github.com/user-attachments/assets/bdf0eaaa-cd5d-4990-b7ec-9c8aa367bc87" />
<img width="1917" height="867" alt="image" src="https://github.com/user-attachments/assets/6ff83645-23aa-4d5e-947c-471862d17efa" />
<img width="1912" height="868" alt="image" src="https://github.com/user-attachments/assets/fac2a2e6-6f55-417b-946b-2c2623356530" />

## Features
- User authentication (Registration and Login) using JWT
- Authenticated users can play the game by submitting number guesses
- A leaderboard to display the top scores/fewest attempts
- Users can reset their game to start over
- Responsive, modern frontend UI

## Tech Stack
- **Frontend**: React (Vite), Tailwind CSS, React Router DOM, Axios
- **Backend**: Node.js, Express, jsonwebtoken, bcryptjs, cors
- **Database**: MongoDB (via Mongoose)

## Deployed Link
[Live Demo](https://guess-the-number-game123.netlify.app)

## Setup Instructions

### Prerequisites
- Node.js (v16+ recommended)
- MongoDB (local instance or MongoDB Atlas)

### 🔧 Backend Setup
Navigate to the backend directory:
```bash
cd game
```
Install dependencies:
```bash
npm install
```
Create a `.env` file in the backend directory:
```env
PORT=8080
MONGO_URI=mongodb://localhost:27017/guess-the-number
JWT_SECRET=your_jwt_secret_here
```
Start the backend server:
```bash
npm start
```

### 💻 Frontend Setup
Navigate to the frontend directory:
```bash
cd game-frontend
```
Install dependencies:
```bash
npm install
```
Start the frontend app:
```bash
npm run dev
```
Visit the app in your browser:  
`http://localhost:5173`

## API Endpoints

### 👤 User Auth Routes
- `POST /api/auth/register` – Register a new user
- `POST /api/auth/login` – Login a user and receive a JWT

### 🎮 Game Routes (Protected)
- `POST /api/game/guess` – Submit a number guess
- `GET /api/game/leaderboard` – Retrieve the game leaderboard
- `PATCH /api/game/reset` – Reset the user's current game

## Notes
- Game routes are protected and require a valid JWT token via headers or cookies to access.
- The frontend is built with React and styled using Tailwind CSS for a modern look.
- Axios is used for API communication between the frontend and backend.
