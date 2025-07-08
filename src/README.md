# Mergington High School Activities

A comprehensive web application for managing extracurricular activities at Mergington High School. The system provides teacher authentication, advanced filtering, and complete activity management capabilities.

## Features

### Activity Management
- View all available extracurricular activities with detailed information
- Advanced search and filtering options:
  - Filter by day of the week (Monday-Sunday)
  - Filter by time slots (morning, afternoon, weekend)
  - Filter by activity categories (sports, academic, arts, technology, community)
  - Text search across activity names and descriptions
- Real-time participant count and capacity tracking

### Teacher Authentication
- Secure login system for teachers and administrators
- Role-based access control (teacher, admin)
- Session management with automatic validation
- Teacher-only registration capabilities

### Student Registration
- Teachers can register students for activities using email addresses
- Teachers can unregister students from activities
- Automatic validation to prevent duplicate registrations
- Activity capacity enforcement

### User Interface
- Responsive web design optimized for desktop and mobile
- Interactive modal dialogs for seamless registration
- Real-time feedback messages for user actions
- Intuitive sidebar navigation with filter controls

### Technical Features
- RESTful API architecture with comprehensive endpoints
- MongoDB database for persistent data storage
- FastAPI backend with automatic API documentation
- Static file serving for frontend assets

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/activities` | Get all activities with optional day/time filtering |
| GET | `/activities/days` | Get list of days with scheduled activities |
| POST | `/activities/{name}/signup` | Register a student for an activity (teacher auth required) |
| POST | `/activities/{name}/unregister` | Unregister a student from an activity (teacher auth required) |
| POST | `/auth/login` | Teacher login endpoint |
| GET | `/auth/check-session` | Validate user session |

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
