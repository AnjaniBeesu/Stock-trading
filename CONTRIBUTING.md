# Contributing

Thank you for considering a contribution to Stock Trading Dashboard! Contributions such as bug fixes, documentation improvements, and thoughtful feature suggestions are welcome.

## Before You Start

1. Read the [README](README.md) to understand the project and its three application areas: `backend/`, `Dashboard/`, and `Frontend/`.
2. Check existing issues and pull requests to avoid duplicating work.
3. For substantial changes, open or comment on an issue to discuss the proposed approach before investing significant effort.
4. Review the [Code of Conduct](CODE_OF_CONDUCT.md) and [Security Policy](SECURITY.md).

## Reporting Bugs and Suggesting Features

- Use GitHub Issues for reproducible bugs and feature proposals.
- Search existing issues first.
- For bugs, include steps to reproduce, expected behavior, actual behavior, and relevant environment details.
- For feature requests, explain the problem and the proposed benefit.
- Do not include credentials, tokens, private user data, or vulnerability details in public issues. Follow the [Security Policy](SECURITY.md) for security reports.

## Development Setup

### Prerequisites

- Git
- Node.js and npm
- MongoDB, either a local instance or MongoDB Atlas

### Clone and Install

Fork the repository, then clone your fork:

```bash
git clone https://github.com/<your-username>/Stock-trading.git
cd Stock-trading
```

Install dependencies separately in each application directory:

```bash
cd backend
npm install

cd ../Dashboard
npm install

cd ../Frontend
npm install
```

### Environment Configuration

Create a `.env` file in `backend/` with your own local values:

```env
PORT=3000
MONGO_URL=mongodb://127.0.0.1:27017/stock-trading
JWT_SECRET=replace_with_a_local_secret
```

For the Dashboard, configure the API URL if required by the application:

```env
VITE_API_URL=http://localhost:3000
```

Never commit `.env` files, credentials, production connection strings, or secrets.

### Running the Applications

Run each application in a separate terminal:

**Backend**
```bash
cd backend
npm start
```

**Dashboard**
```bash
cd Dashboard
npm run dev
```

**Frontend**
```bash
cd Frontend
npm run dev
```

The Dashboard README documents `npm run build` and `npm run lint` as available checks. Run them from `Dashboard/` when changing that application:

```bash
npm run build
npm run lint
```

No repository-wide test command is documented at this time. If you add or change functionality, run the relevant available checks and manually verify the affected flow. Do not claim tests passed unless you ran them.

## Branches and Pull Requests

1. Create a focused branch from the current default branch:

   ```bash
   git checkout -b type/short-description
   ```

2. Keep the change scoped to one concern and follow the existing code style and directory conventions.
3. Use clear, imperative commit messages, for example:
   - `docs: add contribution guidelines`
   - `fix: handle empty watchlist response`
   - `feat: improve portfolio summary`
4. Before opening a pull request, review your diff, remove debug code, and ensure no secrets or generated files are included.
5. Open a pull request against the upstream repository's default branch. Explain the problem, summarize the implementation, list the checks you ran, and link related issues.
6. Be responsive to review feedback. Maintainers decide whether and when a contribution is merged.

## Coding and Documentation Guidelines

- Follow the conventions already used in the relevant application directory.
- Prefer clear, maintainable changes over unnecessary refactoring.
- Keep documentation accurate and update it when behavior or setup instructions change.
- Do not introduce dependencies without explaining why they are needed.
- Do not commit secrets, local environment files, or personal data.

## Review and Support

Pull requests may be reviewed for correctness, maintainability, scope, and consistency with the project. Submission does not guarantee acceptance or a particular review timeline.

Thank you for helping improve the project!
