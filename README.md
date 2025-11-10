# ACEest_Fitness
## Intro To DevOps Assignment 2

### Steps to Run the App
#### (A) Getting Started Locally
    1. Clone the Repository
      - git clone git@github.com:code-arpit/ACEest_Fitness.git
      - cd ACEest_Fitness/src

    2. Create and Activate a Virtual Environment
      - python -m venv venv
      - source venv/bin/activate

    3. Install Dependencies
      - pip install -r requirements.txt

    4. Run the Flask Application
      - python app.py
      - Open http://localhost:5000 in your browser to use the app.
    
    5. Running Tests Locally
      - All unit tests reside in the tests/ directory and use Pytest.
      - pytest tests/test.py

#### (B) Docker Usage
    Run the app inside a Docker container for portability and consistency.
    1. Build the Docker Image
      - docker build -t fitness_test .

    2. Run the Container
      - docker run -p 5000:5000 fitness_test
      - Open http://localhost:5000 in your browser to use the app.

#### (C) Kubernetes Deployment
    1. Normal Deployment
      - Deploy using kubectl apply -f deployment.yaml
      - Expose with service.yaml for internal/external access.

    2. Advanced Deployment Strategies:
      - Canary Deployment
        - Run parallel stable and canary deployments.
        - Gradually shift traffic towards canary by managing replica counts.
        - Use modified deployment YAMLs with version labels.

      - Blue-Green Deployment
        - Maintain two live environments (blue & green).
        - Switch active environment by changing service selector labels.
        - Enables zero downtime and easy rollback.

#### (D) GitHub Actions CI/CD Pipeline
    With every push or PR to the main branch, GitHub Actions automatically:
      - Builds the Docker image of the app, ensuring dependencies are isolated.
      - Runs Pytest unit tests inside the Docker container.
      - Marks the workflow/build as successful if tests pass.
      - Provides early feedback on build or test failures.

#### (E) Project Overview
    This project implements a robust DevOps pipeline for ACEest Fitness & Gym, involving:
      - Flask-based web application development.
      - Version control with Git and GitHub.
      - Automated testing with Pytest.
      - Containerization using Docker.
      - Kubernetes orchestration with normal, canary, and blue-green deployment strategies.
      - Continuous integration and delivery via GitHub Actions.
      - Ensures code quality, environment consistency, and reliable deployment.

