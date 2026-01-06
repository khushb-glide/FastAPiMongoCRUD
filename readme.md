# FastAPI Mongo Notes App

A simple notes application built using FastAPI and MongoDB.

---

## Features

* Create, read, update, and delete notes
* Explicit save (no auto-save)
* Minimal web interface

---

## Tech Stack

* FastAPI (Python)
* MongoDB
* HTML, CSS, JavaScript
* Pytest

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

## Setup & Run

### Prerequisites

* Python 3.x
* MongoDB running locally

### Environment Variable

```
MONGO_URI=mongodb://localhost:27017
```

### Run

```
uvicorn backend.main:app --reload
```

Open:

```
http://127.0.0.1:8000
```

---

## Testing

```
pytest
```
