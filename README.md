# 🐾 Pet&Pur

*Find your purrfect match!*

We're building **Pet&Pur**, a pet-friendly dating web application that brings people together through romantic compatibility, shared interests, and their love for animals.

As part of the **42 Matcha project**, we want to explore a more inclusive and personalised approach to online dating. Our goal is to create a platform where people can find meaningful connections while considering not only their romantic preferences but also their lifestyles, pets, allergies, and animal-related dealbreakers.

We believe that finding the right match goes beyond two people getting along — their furry (or not-so-furry) companions matter too!

## 🛠️ Tech Stack

We're planning to build Pet&Pur using the following technologies:

| Component | Technology |
|---|---|
| Frontend | React (planned) |
| Backend | Rust |
| Database | PostgreSQL |
| Web Server | Caddy |
| Containerisation | Docker & Docker Compose |
| Version Control | Git & GitHub |
| CI/CD | GitHub Actions |

## 📋 Prerequisites

Before getting started, we'll need:

- Git
- Docker and Docker Compose
- Rust and Cargo (for local backend development)
- Node.js and npm (for local frontend development)

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/gltats/Pet-Pur.git
cd Pet-Pur
```

### 2. Environment configuration

We'll document the required environment variables as we develop the application.

We'll keep sensitive information, such as passwords, API keys, and database credentials, out of version control by using local `.env` files. Please refer to .env example.

### 3. Run the application (planned)

Once we've configured our Docker environment, we'll be able to start our services using:

```bash
docker compose up --build
```

Our application will consist of four containerised services: React, Rust, Caddy, and PostgreSQL.

## 🌿 GitHub Workflow

To keep our development organised and maintain code quality, we've decided to follow a **branch-based workflow with pull requests**.

Our `main` branch is protected, meaning we won't push changes directly to it.

### Branch Naming

We'll use descriptive branch names following this convention:

```text
type/short-description
```

Examples:

```text
feat/user-authentication
fix/login-validation
chore/project-setup
ci/github-actions
docs/update-readme
```

### Conventional Commits

We'll follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification to keep our commit history clear and consistent.

**Format:**

```text
type(scope): short description
```

| Type | Purpose |
|---|---|
| `feat` | Introduce a new feature |
| `fix` | Fix a bug |
| `chore` | Maintenance or project setup |
| `ci` | GitHub Actions and CI configuration |
| `build` | Build system, Docker, or dependencies |
| `docs` | Documentation changes |
| `refactor` | Improve code without changing behaviour |
| `style` | Code formatting (not UI styling) |
| `test` | Add or update tests |
| `perf` | Performance improvements |

Examples:

```bash
git commit -m "feat(auth): add user registration"
git commit -m "fix(api): handle invalid requests"
git commit -m "ci: configure automated linting"
```

### Pull Requests

We've established the following process:

1. We'll create a new branch from the latest `main`.
2. We'll commit our changes following Conventional Commits.
3. We'll open a pull request for review.
4. We'll ensure that all required automated checks pass.
5. We'll review each other's code and require one approval before merging.
6. We'll resolve review discussions before merging.
7. We'll use **Squash and Merge** to maintain a clean commit history.

## ✅ Code Quality & Linting

We want to maintain consistent coding standards throughout the project. To achieve this, we're planning to integrate automated formatting, linting, and testing.

| Component | Tool | Purpose |
|---|---|---|
| Rust | rustfmt | Formatting |
| Rust | Clippy | Static analysis |
| Rust | Cargo Test | Automated tests |
| React | ESLint | Code quality |
| React | Build check | Verify compilation/build |
| Caddy | Caddy validation | Server configuration |
| Docker | Docker Compose | Configuration validation |

Diference between Rustfmt, Clippy and Cargo
| Rust tools | What it checks |
|rustfmt | Is the code formatted consistently? |
|Clippy | Are we using suspicious, inefficient, or unnecessarily complicated patterns? |
|cargo test | Does the code behave the way we intended? |

### Local Checks (once configured)

**Rust:**

```bash
cd backend
cargo fmt --all -- --check
cargo clippy --all-targets -- -D warnings
cargo test
```

**React:**

```bash
cd frontend
npm run lint
npm run build
```

**Docker Compose:**

```bash
docker compose config --quiet
```

### GitHub Actions

We'll use GitHub Actions to automate our code quality checks whenever we open or update a pull request.

Once configured as required status checks, these validations will help us prevent changes that don't meet our standards from being merged into `main`.

## 🤖 AI-Assisted Development

We're also incorporating AI-assisted development and code reviews into our workflow.

We'll maintain project-specific guidelines in:

- `.github/copilot-instructions.md` — GitHub Copilot instructions.
- `AGENTS.md` — General instructions for compatible AI coding agents.

We'll use AI tools to support our development process, but we'll remain responsible for understanding, testing, and reviewing the code we contribute.

## 🔒 Security & Privacy

As we're building a dating application that handles personal information, we want to prioritise security and privacy from the beginning.

We'll aim to:

- Protect credentials and sensitive information.
- Validate user inputs and file uploads.
- Prevent common security vulnerabilities.
- Implement secure authentication and authorisation.
- Restrict database access to authorised services.
- Respect GDPR requirements and users' privacy.

## 📌 Project Status

**Current phase:** Initial setup and architecture planning.

We're currently establishing our repository structure, development environment, and collaboration workflow.

We'll expand this documentation as our application takes shape.