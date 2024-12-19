# Getting Started with Kitchen Canvas Development

## Prerequisites
- Node.js (v18+)
- PostgreSQL (v14+)
- Git
- VS Code (recommended)

## Development Environment Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/kitchen-canvas.git
cd kitchen-canvas
```

### 2. Install Dependencies
```bash
# Install frontend dependencies
cd frontend
npm install

# Install backend dependencies
cd ../backend
npm install
```

### 3. Environment Configuration
```bash
# Copy example env files
cp .env.example .env
```

Edit `.env` with your local settings:
```env
DATABASE_URL=postgresql://user:password@localhost:5432/kitchen_canvas
JWT_SECRET=your-secret-key
API_KEY_SPOONACULAR=your-api-key
```

### 4. Database Setup
```bash
# Run migrations
npm run prisma:migrate

# Seed initial data
npm run prisma:seed
```

### 5. Start Development Servers
```bash
# Start frontend (in frontend directory)
npm run dev

# Start backend (in backend directory)
npm run dev
```

## Development Workflow

1. Create a new branch for your feature/fix
```bash
git checkout -b feature/your-feature-name
```

2. Make your changes and commit using conventional commits:
```bash
git commit -m "feat: add user authentication"
git commit -m "fix: resolve recipe loading issue"
```

3. Push and create a PR
```bash
git push origin feature/your-feature-name
```

## Code Quality Checks

Run before submitting PRs:
```bash
# Lint code
npm run lint

# Run tests
npm run test

# Type checking
npm run type-check
```

## Useful Commands

```bash
# Generate Prisma types
npm run prisma:generate

# Run e2e tests
npm run test:e2e

# Build for production
npm run build
```

## Getting Help

- Check our [Troubleshooting Guide](../user/troubleshooting.md)
- Ask in the #dev-help Slack channel
- Tag maintainers in your PR for review 