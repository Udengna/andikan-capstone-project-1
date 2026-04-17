This guide will help you set up and contribute to the project in under 1 hour.

Prerequisites

Ensure you have the following installed:

- Python 3.10+
- pip (Python package manager)
- Git

1. Clone the Repository

git clone <your-repo-url>
cd your-repo-name

2. Install Dependencies
pip install -r requirements.txt

3. Run the Application
python app.py

4. Run Tests
pytest -v

5. Create a Feature Branch

All work must be done on a feature branch.

6. Make Changes & Commit

Follow the commit convention: git commit -m "[TRELLO-###] Short description"

7. Push Changes
git push origin feature/TRELLO-###-description

8. Create a Pull Request
Go to GitHub
Open a Pull Request (PR)
Ensure:
CI checks pass
PR title includes Trello ID

9. CI/CD Checks

Every PR triggers:

Dependency installation
Linting (flake8)
Tests (pytest)

If any check fails:

Fix the issue locally
Commit and push again
Troubleshooting
Tests failing?
pytest -v
Lint errors?
flake8 app.py test_app.py
Dependency issues?
pip install -r requirements.tx

