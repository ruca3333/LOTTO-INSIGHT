# Contributing to LottoInsight

Thank you for your interest in contributing to LottoInsight! This document provides guidelines and instructions for contributing to the project.

## Code of Conduct

We are committed to providing a welcoming and inclusive environment. All contributors are expected to:

- Be respectful and constructive
- Welcome feedback and criticism
- Focus on what is best for the community
- Show empathy towards other community members

## Getting Started

### 1. Fork the Repository

```bash
git clone https://github.com/YOUR_USERNAME/LOTTO-INSIGHT.git
cd LOTTO-INSIGHT
```

### 2. Create a Feature Branch

```bash
git checkout -b feature/your-feature-name
```

Branch naming convention:
- `feature/` - New features
- `fix/` - Bug fixes
- `docs/` - Documentation updates
- `refactor/` - Code refactoring
- `test/` - Test additions

### 3. Make Your Changes

Ensure your code follows our style guidelines:

#### JavaScript/TypeScript
```bash
npm run format  # Prettier
npm run lint    # ESLint
```

#### Python
```bash
black .
pylint src/
```

### 4. Commit Messages

Use Conventional Commits:

```
feat: add hot number tracking to dashboard
fix: resolve timezone issue in countdown timer
docs: update API documentation
refactor: simplify prediction engine logic
test: add unit tests for heatmap calculation
```

### 5. Push and Create Pull Request

```bash
git push origin feature/your-feature-name
```

Then create a PR with:
- Clear title
- Detailed description
- Link to related issues
- Screenshots (if UI changes)
- Tests added/updated

## Development Guidelines

### Frontend

- Use functional components with hooks
- Follow Material Design 3 principles
- Ensure accessibility (WCAG 2.1)
- Write responsive designs (mobile-first)
- Use TypeScript for type safety

### Backend

- Follow RESTful API standards
- Add comprehensive error handling
- Include input validation
- Write unit tests (>80% coverage)
- Document all endpoints

### Scraper

- Handle rate limiting gracefully
- Log all activities
- Implement retry logic
- Test against staging URLs first
- Document data schema

## Testing

All contributions must include tests:

```bash
# Run tests
npm test           # JavaScript
pytest             # Python

# Check coverage
npm run coverage   # JavaScript
pytest --cov       # Python
```

## Documentation

Update relevant documentation:

- **Code changes**: Update docstrings and comments
- **API changes**: Update API.md
- **Architecture changes**: Update ARCHITECTURE.md
- **Setup changes**: Update README.md

## Pull Request Process

1. **Before submitting**:
   - Run all tests
   - Run linter and formatter
   - Update documentation
   - Test manually if applicable

2. **PR checklist**:
   - [ ] Code follows style guidelines
   - [ ] Tests added/updated
   - [ ] Documentation updated
   - [ ] No breaking changes (or documented)
   - [ ] Screenshots included (if UI changes)

3. **Review process**:
   - At least 2 approvals required
   - All CI checks must pass
   - Conversations resolved

4. **Merge**:
   - Squash commits for cleanliness
   - Use meaningful commit message
   - Delete branch after merge

## Reporting Bugs

Use the bug report template:

```markdown
**Description**: Clear and concise description

**Steps to Reproduce**:
1. Step one
2. Step two
3. Step three

**Expected Behavior**: What should happen

**Actual Behavior**: What actually happens

**Environment**:
- OS: [e.g., macOS, Windows]
- Node version: [e.g., 18.0.0]
- Browser: [e.g., Chrome 120]

**Screenshots**: If applicable
```

## Feature Requests

Use the feature request template:

```markdown
**Is your feature related to a problem?**
Clear description of the problem

**Describe the solution**
Clear description of the desired solution

**Describe alternatives**
Any alternative approaches

**Additional context**
Any other relevant context
```

## Getting Help

- **Questions**: Use GitHub Discussions
- **Bugs**: Open an Issue
- **Ideas**: Start a Discussion

## Recognition

Contributors will be recognized in:
- README.md contributors section
- Release notes
- Our website (coming soon)

Thank you for contributing! 🎉