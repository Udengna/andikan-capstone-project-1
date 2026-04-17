
Thank you for contributing to this project! This guide outlines the workflow, standards, and rules for contributing.

Development Workflow

1. Pick a task from Trello (TRELLO-###)
2. Move the card to **In Progress**
3. Create a feature branch
4. Implement changes
5. Commit with proper format
6. Open a Pull Request
7. Wait for CI checks
8. Get approval and merge
9. Move card to **Done**

Branching Strategy

- `main` → Stable production-ready code 
- `feature/TRELLO-###-description` → Feature branches 

Commit Convention

All commits must include the Trello ID:

Pull Request Process

- PR must be created for all changes 
- No direct pushes to `main` 
- PR title must include Trello ID 

### Requirements:
- CI must pass 
- Code must be reviewed 
- All comments must be resolved 

CI/CD Pipeline

The project uses GitHub Actions for Continuous Integration.

### Pipeline Steps:
1. Install dependencies 
2. Run flake8 (linting) 
3. Run pytest (testing) 

### Rules:
- Failed lint = failed build 
- Failed test = failed build 
- Merge is blocked until CI passes 

Coding Standards

- Follow Python best practices 
- Ensure code passes flake8 
- Keep functions simple and readable 
- Write meaningful variable names 

Failure Handling

If CI fails:

1. Check logs in GitHub Actions 
2. Fix the issue locally 
3. Re-run tests:pytest 
4. Fix lint issues
5. Commit and push again

Testing Requirements
Minimum 8 tests required
All tests must pass
Include edge cases
Do not merge broken tests

Trello Integration
Each task must have a Trello ID
Cards must move across workflow stages
Link PRs to Trello cards
