# Development Guide

## Initial Setup

This project is best developed using GitHub Codespaces, which provides a consistent development environment with all the necessary tools pre-configured.

### Setting up your development environment

1. Open the repository in a codespace
2. Wait for the container to finish building and installing dependencies
3. Install Python dependencies by running:

   ```bash
   python -m pip install -r requirements.txt
   ```

### Dependencies

The project requires the following Python packages:

- **FastAPI** - Modern web framework for building APIs
- **Uvicorn** - ASGI server implementation for running the FastAPI application
- **PyMongo** - MongoDB driver for Python
- **Argon2** - Secure password hashing library

These dependencies will be installed when you run `pip install -r requirements.txt`

## Debugging

### Running the website locally

1. From VS Code's Run and Debug view (Ctrl+Shift+D), select "Launch Mergington WebApp" from the launch configuration dropdown
2. Press F5 or click the green play button to start debugging
3. The website will be available at `http://localhost:8000`
4. The API documentation will be available at `http://localhost:8000/docs`

### Debugging tips

- FastAPI's auto-reload feature will automatically restart the server when you make code changes
- Use the interactive API documentation at `/docs` to test your endpoints

## Getting Started

1. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

2. Run the application:

   ```bash
   uvicorn app:app --reload
   ```

3. Open your browser and go to:
   - Website: http://localhost:8000
   - API documentation: http://localhost:8000/docs
   - Alternative documentation: http://localhost:8000/redoc

## Usage

### API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/activities` | Get all activities with optional filtering by day/time |
| GET | `/activities/days` | Get available days with activities |
| POST | `/activities/{name}/signup` | Register student for activity (auth required) |
| POST | `/activities/{name}/unregister` | Remove student from activity (auth required) |
| POST | `/auth/login` | Teacher/admin authentication |
| GET | `/auth/check-session` | Validate session |

> [!IMPORTANT]
> Data is stored in MongoDB. If running without MongoDB, the app will attempt to connect to localhost:27017.
