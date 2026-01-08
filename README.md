 GitHub Repository Tracker API

A FastAPI-based REST API that integrates with the GitHub REST API to fetch repository details and store them in a database.
The application supports full CRUD operations and follows clean backend design principles.

 Tech Stack

* FastAPI – API framework
* SQLAlchemy – ORM for database operations
* Pydantic – Request/response validation
* SQLite / PostgreSQL – Database
* Pytest – Testing framework
* GitHub REST API – External data source

 Features

* Fetch repository details from GitHub
* Store repository information in database
* Create, read, update, and delete repositories
* Input validation and structured responses
* Error handling for missing resources
* Automated API documentation (`/docs`)

 API Endpoints

| Method | Endpoint      | Description                   |
| ------ | ------------- | ----------------------------- |
| POST   | `/repos`      | Fetch repo from GitHub & save |
| GET    | `/repos/{id}` | Get repo by ID                |
| PUT    | `/repos/{id}` | Update star count             |
| DELETE | `/repos/{id}` | Delete repo                   |

 How to Run

```bash
pip install -r requirements.txt
uvicorn app.main:app --reload
`http://127.0.0.1:8000/docs`

 Testing

* Uses **FastAPI TestClient**
* In-memory SQLite database
* Covers all CRUD operations


 Limitations

* No authentication
* GitHub API rate limits not handled
* SQLite used for simplicity


 Improvements

* GitHub token authentication
* Docker + PostgreSQL
* Async database support
* Caching & pagination


