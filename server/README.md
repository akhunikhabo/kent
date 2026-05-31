# Kent Server

Node.js/Express backend for the Kent video platform.

## Setup

1. Install dependencies:
   ```bash
   npm install
   ```

2. Create `.env` file (copy from `.env.example`):
   ```bash
   cp .env.example .env
   ```

3. Configure PostgreSQL and update `.env` with your database credentials

4. Run database migrations:
   ```bash
   npm run migrate
   ```

5. Start the server:
   ```bash
   npm run dev
   ```

Server will run on `http://localhost:5000`

## API Endpoints

### Auth
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user

### Videos
- `GET /api/videos` - Get all videos
- `GET /api/videos/:id` - Get video by ID
- `POST /api/videos/upload` - Upload new video (requires auth)

### Users
- `GET /api/users/profile` - Get user profile (requires auth)
- `GET /api/users/videos` - Get user's videos (requires auth)
- `GET /api/users/history` - Get watch history (requires auth)
