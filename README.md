# CIRS — Campus Item Recovery System

A campus lost-and-found application built with React, Vite, Express, MongoDB, and Mongoose.

## Requirements

- Node.js 20+
- MongoDB (local or hosted)

## Configure and run

1. Copy `backend/.env.example` to `backend/.env` and set `MONGODB_URI` and `JWT_SECRET`. Copy `frontend/.env.example` to `frontend/.env` only if you need to change the API URL.
2. Install dependencies:

   ```sh
   npm install
   Set-Location backend
   npm install
   Set-Location ..\frontend
   npm install
   Set-Location ..
   ```

3. Start the API and frontend together:

   ```sh
   npm run dev
   ```

   Vite runs at `http://localhost:5173` and the API runs at `http://localhost:5000`.

4. Create an account, then report and manage your campus items.

For production, build the frontend with `npm run build` and start the API with `npm start`.

## API overview

- `POST /api/auth/register`, `POST /api/auth/login`, `GET /api/auth/me`
- `GET /api/items`, `POST /api/items`, `GET /api/items/:id`
- `GET /api/items/:id/matches`, `PATCH /api/items/:id`, `DELETE /api/items/:id`
- `GET /api/items/stats`
- `GET /api/profile`, `PATCH /api/profile`

Uploaded images are served from `/uploads`. Set `CLIENT_URL` if the frontend is hosted on another origin.
