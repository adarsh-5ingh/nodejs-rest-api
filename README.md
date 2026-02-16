# Node.js REST API

A production-ready RESTful API boilerplate using Node.js, Express, MongoDB (Mongoose), and JWT authentication.

## Features
- Modular Express architecture
- Secure JWT-based authentication
- User CRUD with validation and hashed passwords
- Environment-based config (.env)
- Ready for Docker, CI/CD, and cloud deployment

## Tech Stack
- Node.js 20+
- Express 5
- MongoDB
- Mongoose
- JWT (HS256)
- Docker
- GitHub Actions (CI/CD)

## Quick Start
```sh
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
npm install
cp .env.example .env # configure secrets
npm start
```

## API
- `POST /api/users/register` — Register
- `POST /api/users/login` — Login (returns JWT)
- `GET /api/users` — List users (auth)
- `GET /api/users/:id` — Get user (auth)
- `PUT /api/users/:id` — Update user (auth)
- `DELETE /api/users/:id` — Delete user (auth)

> Auth endpoints return JWT. Use `Authorization: Bearer <token>` for protected routes.

## Docker
This project is fully containerized for portability and consistency.

**How to use:**
```sh
# Build the Docker image
docker build -t nodejs-rest-api .

# Run the app in a container
# (Make sure you have a .env file with your secrets)
docker run -p 3000:3000 --env-file .env nodejs-rest-api
```

## License
MIT
