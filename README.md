# FilmLog — Frontend Companion

A modern movie watchlist and review platform interface designed for the GDGoC Movie Watchlist backend.

Built with Vite, Tailwind CSS, and Modern JavaScript.

---

## Configuration

The frontend connects to the backend API via the `VITE_API_BASE_URL` environment variable.

Create a `.env` file in the root directory:
```env
VITE_API_BASE_URL="<your-backend-api-url>"
```

You can also dynamically change the connected backend URL directly inside the application UI via the **Settings (gear icon)** modal in the navigation bar.

---

## Getting Started

### 1. Install Dependencies
```bash
npm install
```

### 2. Start Development Server
```bash
npm run dev
```

### 3. Build for Production
```bash
npm run build
```

### 4. Preview Production Build
```bash
npm run preview
```

---

## Features

1. **Discover Movies (`GET /api/movies`)**:
   - Browse catalog with poster, rating, director, and genre tags.
   - Filter by title/director and genre pills.
   - Shuffle / randomize catalog display.

2. **Movie Details (`GET /api/movies/:id`)**:
   - Full movie synopsis, duration, director, and cast list.

3. **Authentication (`POST /api/auth/register` & `POST /api/auth/login`)**:
   - Register and login modal.
   - JWT token storage in `localStorage` sent via `Authorization: Bearer <token>`.

4. **Watchlist (`GET /api/watchlist`, `POST /api/watchlist`, `DELETE /api/watchlist/:id`)**:
   - Add/remove movies to personal watchlist.

5. **Watched & Reviews (`GET /api/watched`, `POST /api/watched`)**:
   - Log watched movies with 1-5 star ratings and written reviews.

6. **AI Movie Recommendation (`POST /api/movies/recommend`)**:
   - Input mood or description to receive grounded movie recommendation from Google Gemini.

7. **API Inspector Drawer**:
   - Real-time logging of HTTP method, URL, status code, and latency.
