# FastAPI Clean Architecture Todo API

A production-ready Todo API built with FastAPI following clean architecture principles and best practices.

## 🏗️ Architecture

This project follows clean architecture principles, with clear separation of:

- **Entities** - Core business objects (`User`, `Todo`)
- **Use Cases** - Application business rules in services
- **Controllers** - HTTP request handlers
- **Infrastructure** - Database, authentication, and external interfaces

## 🔑 Key Features

- Complete CRUD operations for Todos
- User authentication with JWT
- Password hashing with bcrypt
- Rate limiting
- PostgreSQL database with SQLAlchemy ORM
- Comprehensive test suite
- Docker support
- Clean code structure following best practices

## 🚀 Getting Started

### Prerequisites

- Python 3.12+
- Docker and Docker Compose (optional)
- PostgreSQL (if running without Docker)

### Running with Docker

```bash
# Start the application and database
docker-compose up
```

The API will be available at `http://localhost:8000`

### Local Development Setup

```bash
# Create a virtual environment
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements-dev.txt

# Configure environment variables
cp .env.example .env     # Update with your values

# Run the application
uvicorn src.main:app --reload
```

## 📝 API Documentation

Once running, view the interactive API documentation at:

- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`

### Key Endpoints

- `POST /auth/` - Register new user
- `POST /auth/token` - Login and get access token
- `GET /todos/` - List all todos
- `POST /todos/` - Create new todo
- `GET /todos/{id}` - Get single todo
- `PUT /todos/{id}` - Update todo
- `DELETE /todos/{id}` - Delete todo
- `PUT /todos/{id}/complete` - Mark todo as complete

## 🧪 Testing

```bash
# Run all tests
pytest

# Run with coverage
pytest --cov=src
```

## 🛠️ Project Structure

```
src/
├── auth/           # Authentication logic
├── database/       # Database configuration
├── entities/       # Domain entities
├── todos/          # Todo feature module
├── users/          # User feature module
├── exceptions.py   # Custom exceptions
├── logging.py      # Logging configuration
└── main.py         # Application entry point
```

## 🔒 Security Features

- JWT authentication
- Password hashing with bcrypt
- Rate limiting on registration endpoint
- CORS protection
- Input validation with Pydantic

## 🤝 Contributing

1. Fork the repository
2. Create a new branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.