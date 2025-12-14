# SmartDine

SmartDine is an intelligent, AI-powered restaurant recommendation and social dining application. It combines natural language processing with geolocation services to help users find the perfect place to eat based on their mood, cravings, and location, while connecting them with friends for a shared dining experience.

## Project Structure

This repository contains both the frontend and backend codebases:

-   **`frontend/smartdine`**: The user interface built with React and Vite.
-   **`backend`**: The server-side logic built with Node.js and Express.

## Tech Stack

### Frontend
-   **Framework**: React (v19) with Vite
-   **Maps**: Leaflet / React-Leaflet
-   **State/API**: Axios, Context API
-   **Styling**: CSS Modules
-   **Services**: Firebase, Supabase Client

### Backend
-   **Runtime**: Node.js
-   **Framework**: Express.js
-   **AI/LLM**: OpenRouter (Google Gemini 2.0 Flash)
-   **Database**: Supabase (PostgreSQL), Local JSON (for MVP data)
-   **Utilities**: Nodemon, Dotenv, Cors

## Features

-   **AI Discovery**: Search for restaurants using natural language queries (e.g., "cheap veg biryani near me").
-   **Social Dining**: Add friends, chat in real-time, and see where friends are dining.
-   **Interactive Maps**: Visualize restaurant locations and plan routes.
-   **User Profiles**: personalized preferences and dining history.
-   **Responsive Design**: Optimized for both mobile and desktop experiences.

## Getting Started

### Prerequisites
-   Node.js (v14 or higher)
-   npm (Node Package Manager)

### 1. Backend Setup

1.  Navigate to the backend directory:
    ```bash
    cd backend
    ```

2.  Install dependencies:
    ```bash
    npm install
    ```

3.  Configure Environment Variables:
    -   Create a `.env` file in the `backend` directory.
    -   Add the following variables (refer to `.env.example`):
        ```env
        OPENROUTER_API_KEY=your_openrouter_key
        OPENROUTER_MODEL=google/gemini-2.0-flash-exp:free
        PORT=4000
        ```

4.  Start the Backend Server:
    ```bash
    npm run dev
    ```
    The server will run on `http://localhost:4000`.

### 2. Frontend Setup

1.  Navigate to the frontend directory:
    ```bash
    cd frontend/smartdine
    ```

2.  Install dependencies:
    ```bash
    npm install
    ```

3.  Configure Environment Variables:
    -   Create a `.env` file in the `frontend/smartdine` directory.
    -   Add the following variables:
        ```env
        VITE_API_URL=http://localhost:4000
        VITE_SUPABASE_URL=your_supabase_url
        VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
        ```

4.  Start the Frontend Application:
    ```bash
    npm run dev
    ```
    The application will launch on `http://localhost:5173`.

## Deployment

### Frontend
The frontend can be deployed to static hosting services like **Vercel**, **Netlify**, or **Render**. Ensure you verify the build command (`npm run build`) and set the environment variables in your hosting dashboard.

### Backend
The backend can be deployed to Node.js hosting providers like **Render**, **Railway**, or **Heroku**. Make sure to set the `NODE_ENV` to production and configure the environment variables on the server.

---

## License
[MIT](LICENSE)
