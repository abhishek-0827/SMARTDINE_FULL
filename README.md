# SmartDine

## 🚀 Live Deployment

**Frontend (Vercel):** [https://smart-dine-frontend-omega.vercel.app/](https://smart-dine-frontend-omega.vercel.app/)  
**Backend (Render):** Deployed on Render

---

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
-   **AI/LLM**: Llama 3.3 70B Versatile (via Groq)
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
    -   Add the following variables:
        ```env
        # Groq AI Configuration
        GROQ_API_KEY=your_groq_api_key
        GROQ_MODEL=llama-3.3-70b-versatile
        
        # Server Configuration
        PORT=4000
        
        # Supabase Configuration (for social features)
        SUPABASE_URL=your_supabase_url
        SUPABASE_ANON_KEY=your_supabase_anon_key
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
        # Backend API
        VITE_API_URL=http://localhost:4000
        
        # Supabase Configuration
        VITE_SUPABASE_URL=your_supabase_url
        VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
        
        # Firebase Configuration (for authentication)
        VITE_FIREBASE_API_KEY=your_firebase_api_key
        VITE_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
        VITE_FIREBASE_PROJECT_ID=your_firebase_project_id
        VITE_FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
        VITE_FIREBASE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
        VITE_FIREBASE_APP_ID=your_firebase_app_id
        
        # EmailJS Configuration (for contact form)
        VITE_EMAILJS_SERVICE_ID=your_emailjs_service_id
        VITE_EMAILJS_TEMPLATE_ID=your_emailjs_template_id
        VITE_EMAILJS_PUBLIC_KEY=your_emailjs_public_key
        ```

4.  Start the Frontend Application:
    ```bash
    npm run dev
    ```
    The application will launch on `http://localhost:5173`.

### Frontend
The frontend is deployed on **Vercel**. Set all environment variables in your Vercel dashboard.

### Backend
The backend is deployed on **Render**. Set `NODE_ENV` to production and configure all environment variables.

---

## License
[MIT](LICENSE)
