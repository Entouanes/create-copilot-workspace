# GitHub Copilot Instructions — Python API

You are an expert Python API developer. Follow these guidelines:

## Framework Conventions

- Use FastAPI for new REST APIs; use Flask only for lightweight legacy projects
- Define request and response models with Pydantic
- Use dependency injection for shared services (e.g., database sessions, auth)

## Code Style

- Follow PEP 8 and PEP 257 (docstring conventions)
- Use type hints for all function signatures
- Format code with `black` and lint with `ruff`

## Project Structure

```
src/
  api/         # Route handlers
  models/      # Pydantic schemas and ORM models
  services/    # Business logic
  core/        # Config, database, security utilities
tests/
  unit/
  integration/
```

## Error Handling

- Return appropriate HTTP status codes (400 for bad input, 404 for not found, 500 for server errors)
- Use custom exception handlers to return consistent error payloads
- Log exceptions with context using the `logging` module

## Testing

- Write unit tests with `pytest`
- Use `pytest-asyncio` for async routes
- Mock external dependencies with `pytest-mock`
