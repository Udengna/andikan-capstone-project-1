GitOps Workflow Project

Project Overview

This project implements a lightweight Flask-based API with a fully automated GitOps workflow. The goal is to demonstrate professional software engineering practices, including task tracking, version control, CI/CD automation, and structured team onboarding.

The API provides simple endpoints for health checks, arithmetic operations, and string manipulation, while the surrounding workflow ensures code quality, traceability, and reliability.

Architecture

This project follows a GitOps-style workflow, where GitHub acts as the single source of truth.

Components:
Trello → Task tracking and workflow management
GitHub → Source control and collaboration
GitHub Actions → CI pipeline (lint + test enforcement)

Workflow Description

1. Tasks are created in Trello with unique IDs (TRELLO-###)
2. Developer creates a feature branch:feature/TRELLO-###-description
3. Code is committed using:[TRELLO-###] commit message
4. A Pull Request (PR) is opened to `main`
5. GitHub Actions automatically runs:
- Dependency installation
- Linting (flake8)
- Testing (pytest)
6. If CI fails → merge is blocked 
7. If CI passes → PR is reviewed and merged
8. Task is moved to 'Done' in Trello 

Commit Conventions

All commits follow this format: [TRELLO-###] Short description

Reflection
1. Why GitOps improves team reliability

GitOps improves reliability by making Git the single source of truth for all changes. Every modification to the codebase is tracked, reviewed, and version-controlled, which reduces ambiguity and prevents unauthorized or untested changes from being introduced. By enforcing structured workflows such as pull requests and automated CI checks, teams can ensure that only validated code reaches the main branch.

Additionally, GitOps enables reproducibility. Since all configurations and workflows are stored in the repository, any developer can replicate the environment and understand the system without relying on undocumented processes. This reduces onboarding time and minimizes errors caused by inconsistent setups.

Overall, GitOps introduces transparency, accountability, and consistency, which are critical for maintaining reliable systems, especially in collaborative environments.

2. Importance of CI/CD in small teams

CI/CD is especially important in small teams because there are fewer people to manually review and test code. Automation ensures that every change is validated through consistent checks, reducing the risk of bugs entering production. It acts as a safety net that compensates for limited human resources.

Continuous Integration helps catch issues early by running tests and linting on every commit or pull request. This prevents problems from accumulating and becoming harder to fix later. Continuous Delivery ensures that the codebase is always in a deployable state.

For small teams, CI/CD improves efficiency by reducing manual work, increases confidence in code changes, and allows developers to focus on building features rather than debugging avoidable issues.

3. Challenges faced implementing the workflow

One challenge was setting up the CI pipeline correctly, especially ensuring that dependencies were installed properly and that the correct commands were executed in sequence. Small configuration mistakes could cause the entire pipeline to fail.

Another challenge was maintaining consistency between local development and the CI environment. Differences in dependency versions or configurations could lead to tests passing locally but failing in CI.

Additionally, structuring the workflow to align with Trello tasks, commit conventions, and PR requirements required careful planning. Ensuring that every change was traceable across tools added complexity but ultimately improved clarity.

Conclusion

This project demonstrates a complete GitOps workflow integrating task tracking, version control, and CI/CD automation. It ensures code quality, traceability, and efficient collaboration, reflecting real-world engineering practices.
