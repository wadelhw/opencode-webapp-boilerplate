# WebApp Template

## Tech Stack

- Backend: FastAPI
- Frontend: React + TailwindCSS
- CI/CD: GitHub Actions

---

## Quick Start

### Backend

```bash
cd backend
bash ../scaffold-scripts/backend-init.sh
```

### Frontend

```bash
cd frontend
bash ../scaffold-scripts/frontend-init.sh
```

---

## Project Structure

```
backend/
frontend/
docs/
.github/workflows/
AGENTS.md
```

---

## CI/CD

GitHub Actions automatically runs:

- Backend lint + pytest
- Frontend lint + tests

