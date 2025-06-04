# outspeed-cra-fastapi

# Voice Chat App

This project consists of a React frontend and a FastAPI backend.

## Prerequisites
- Node.js and npm
- Python 3.8+
- uv (for python package management)
- Outspeed API key (https://dashboard.outspeed.com)

## Running the Apps

Open two terminal windows/tabs in the project root directory.

### 1. Start the React App
```bash
cd my-app
npm start
```
This will start the React development server at [http://localhost:3000](http://localhost:3000).

### 2. Setup `OUTSPEED_API_KEY`

In the backend, create a .env file and add your `OUTSPEED_API_KEY`

```bash
cd fastapi-backend
cp .env.example .env
```

### 3. Start the FastAPI Backend

Setup the environment

```bash
uv venv
source .venv/bin/activate
uv sync # this will install all packages
```

```bash
dotenv run -- uvicorn main:app --reload --port 8080
```
This will start the FastAPI server at [http://localhost:8080](http://localhost:8080).

---

- Make sure your FastAPI `main.py` is in the root directory or adjust the command accordingly.
- The React app expects the backend to be running at `http://localhost:8080` for the `/token` endpoint.

## Notes
- Update environment variables in your `.env` file as needed.
- For production, consider using build tools and a production server.
