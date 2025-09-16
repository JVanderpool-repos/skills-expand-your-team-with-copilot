# Mergington High School Activities

A comprehensive web application for managing extracurricular activities at Mergington High School. Built with FastAPI backend and modern responsive frontend, this system enables students to discover and register for activities while providing teachers with administrative capabilities.

## Features

### For Students
- **Browse Activities**: View all available extracurricular activities with detailed information
- **Advanced Search & Filtering**: 
  - Search activities by name or description
  - Filter by category (Sports, Arts, Academic, Community, Technology)
  - Filter by day of the week (Monday through Sunday)
  - Filter by time (Before School, After School, Weekend)
- **Activity Details**: View schedules, descriptions, participant limits, and current enrollment
- **Responsive Design**: Works seamlessly on desktop and mobile devices

### For Teachers & Administrators
- **Authentication System**: Secure login for teachers and administrators
- **Student Management**: Register and unregister students for activities
- **Activity Oversight**: Monitor participation and manage enrollments

### Technical Features
- **FastAPI Backend**: Modern, fast API with automatic documentation
- **MongoDB Integration**: Robust data persistence and querying
- **RESTful API**: Well-documented endpoints at `/docs`
- **Secure Authentication**: Password hashing with Argon2
- **Real-time Updates**: Dynamic content loading and filtering

## Activity Categories

The system supports diverse extracurricular activities including:
- **Sports**: Soccer Team, Basketball Team, Morning Fitness
- **Arts**: Art Club, Drama Club
- **Academic**: Math Club, Chess Club, Debate Team, Science Olympiad
- **Technology**: Programming Class, Weekend Robotics Workshop
- **Community**: Various community service activities
- **Special Interest**: Manga Maniacs and other themed clubs

## Architecture

- **Frontend**: Vanilla JavaScript with modern CSS for responsive design
- **Backend**: Python FastAPI with automatic API documentation
- **Database**: MongoDB for scalable data storage
- **Authentication**: Role-based access control for teachers and administrators

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/activities` | Get all activities with optional filtering |
| GET | `/activities/days` | Get available days with activities |
| POST | `/activities/{name}/signup` | Register student for activity (auth required) |
| POST | `/activities/{name}/unregister` | Remove student from activity (auth required) |
| POST | `/auth/login` | Teacher/admin authentication |
| GET | `/auth/check-session` | Validate session |

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).

## Quick Start

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Start the application:
   ```bash
   uvicorn app:app --reload
   ```

3. Access the application:
   - Website: http://localhost:8000
   - API Documentation: http://localhost:8000/docs
