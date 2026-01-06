📝 Notes Web App

A clean, full-stack application for managing personal notes. This project features a high-performance FastAPI backend, a MongoDB NoSQL database for flexible data storage, and a responsive Vanilla JavaScript frontend.

🚀 Features

Complete CRUD Functionality: Create, view, update, and delete notes seamlessly.

Asynchronous Frontend: Uses the modern Fetch API to interact with the backend without full page reloads.

RESTful API Design: Structured endpoints with Pydantic models for request validation.

Robust Data Storage: MongoDB integration via PyMongo for efficient document storage.

Automated Testing: Includes a test suite using pytest to ensure API reliability.

🛠️ Tech Stack

Backend: FastAPI (Python)

Database: MongoDB

Frontend: HTML5, CSS3, Vanilla JavaScript

Server: Uvicorn (ASGI)

Testing: Pytest & HTTPX

📂 Project Structure

├── backend/
│   ├── main.py            # Entry point: FastAPI routes and server config
│   ├── mongo_notes.py     # Database layer: MongoDB CRUD operations
│   └── test_notes_api.py  # Test suite for API endpoints
├── frontend/
│   ├── notes_list.html    # Dashboard view (Lists all notes)
│   ├── notes_edit.html    # Editor view (Create/Edit/Delete notes)
│   ├── notes.js           # Client-side logic and API integration
│   └── styles.css         # Application-wide styling
├── requirements.txt       # Python dependency list
└── .env                   # Configuration for MONGO_URI (Local)


⚙️ Setup & Installation

1. Prerequisites

Python 3.10+

MongoDB installed locally or an Atlas connection string.

2. Configure Environment

Set your MongoDB connection string as an environment variable or add it to a .env file in the root:

# Example for local MongoDB
export MONGO_URI="mongodb://localhost:27017"


3. Install Dependencies

pip install -r requirements.txt


4. Run the Application

Start the development server with auto-reload enabled:

uvicorn backend.main:app --reload


The application will be live at http://127.0.0.1:8000.

🧪 Testing

To run the automated API tests:

pytest backend/test_notes_api.py


🔌 API Reference

Endpoint

Method

Description

/api/notes

GET

Fetch all notes

/api/notes

POST

Create a new note

/api/notes/{id}

GET

Retrieve a single note

/api/notes/{id}

PUT

Update an existing note

/api/notes/{id}

DELETE

Remove a note

