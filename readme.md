# FastAPI Mongo Notes App

A simple notes web application built using **FastAPI** and **MongoDB**.

The project implements basic CRUD functionality with a minimal web UI. The focus was on building a clean backend, correct data flow, and a working end-to-end system rather than spending time on UI polish.

---

## Features

* View all notes
* Create a new note
* Edit an existing note
* Delete a note
* Notes are saved only when explicitly clicking **Save**

---

## Tech Stack

* **Backend:** FastAPI (Python)
* **Database:** MongoDB
* **Frontend:** HTML, CSS, JavaScript (no frameworks)
* **Testing:** Pytest

---

## Project Structure

```
backend/
  main.py          # FastAPI app and routes
  mongo_notes.py   # MongoDB connection and CRUD logic

frontend/
  notes_list.html  # Notes list page
  notes_edit.html  # Note editor page
  styles.css
  notes.js

tests/
  test_notes_api.py

requirements.txt
```

---

## Running the Project

### Prerequisites

* Python 3.x
* MongoDB running locally

### Environment Variable

Set the MongoDB connection string using an environment variable:

```
MONGO_URI=mongodb://localhost:27017
```

### Start the Server

```
uvicorn backend.main:app --reload
```

Open in browser:

```
http://127.0.0.1:8000
```

---

## Testing

Tests are written using **pytest**.

Run all tests with:

```
pytest
```

---

## Notes

* MongoDB data is stored in the `notes_app` database
* Configuration values (like database URLs) are not hardcoded
* The UI is intentionally minimal and functional

---

Built as a focused backend-oriented project to demonstrate API design, database interaction, and basic testing.
