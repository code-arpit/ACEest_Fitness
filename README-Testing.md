# README-Code-Testing.md

## Codebase and Testing
## Project Structure
- ACEest_Fitness.py: Main Flask application code
- /tests: Directory containing Pytest test cases

## Running Tests Locally
- Ensure dependencies installed (pip install -r requirements.txt)
- Run tests using:
    - text
    - pytest

- Testing in CI/CD
    - Tests are automatically triggered on code commits by pipeline
    - Builds fail if tests do not pass

- Writing Tests
    - Use Pytest to cover API endpoints, business logic, input validation
    - Organize tests into multiple test files for modularity

