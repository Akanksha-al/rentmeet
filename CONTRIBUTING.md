# Contributing to RentMeet

Thank you for your interest in contributing to RentMeet! This document provides guidelines and information for contributors.

## Getting Started

1. Fork the repository on GitHub
2. Clone your fork locally:
   ```bash
   git clone https://github.com/yourusername/rentmeet.git
   cd rentmeet
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Start the development server:
   ```bash
   npm run dev
   ```

## Development Guidelines

### Code Style
- Use TypeScript for all new code
- Follow existing naming conventions
- Write meaningful commit messages
- Add comments for complex logic
- Use Prettier for code formatting

### Project Structure
- **Frontend components** go in `client/src/components/`
- **Page components** go in `client/src/pages/`
- **Shared types** go in `shared/schema.ts`
- **API routes** go in `server/routes.ts`
- **Storage logic** goes in `server/storage.ts`

### Making Changes

1. Create a new branch for your feature:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. Make your changes following the project conventions

3. Test your changes thoroughly:
   - Test both frontend and backend functionality
   - Check mobile responsiveness
   - Verify timezone handling works correctly
   - Test social sharing features

4. Commit your changes:
   ```bash
   git commit -m "feat: add your feature description"
   ```

5. Push to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```

6. Create a Pull Request on GitHub

### Commit Message Convention

We use conventional commits:
- `feat:` - New features
- `fix:` - Bug fixes
- `docs:` - Documentation changes
- `style:` - Code style changes (formatting, etc.)
- `refactor:` - Code refactoring
- `test:` - Adding or updating tests
- `chore:` - Maintenance tasks

### Testing

Before submitting a PR:
- [ ] App starts without errors (`npm run dev`)
- [ ] All TypeScript types are correct (no compilation errors)
- [ ] Meeting scheduling works across timezones
- [ ] Social sharing buttons function properly
- [ ] Mobile navigation works correctly
- [ ] Calendar displays meetings properly

### Areas for Contribution

We welcome contributions in these areas:

#### Frontend Features
- Enhanced calendar views (week/month/year)
- Meeting reminder notifications
- User authentication and profiles
- Advanced filtering and search
- Accessibility improvements

#### Backend Features  
- Email notifications
- Calendar integrations (Google, Outlook)
- Multi-language support
- Advanced timezone handling
- API rate limiting

#### Documentation
- Code documentation
- User guides
- API documentation
- Setup tutorials

#### Testing
- Unit tests for components
- Integration tests
- End-to-end testing
- Performance testing

### Feature Requests

For major features:
1. Open an issue first to discuss the idea
2. Get feedback from maintainers
3. Create a detailed implementation plan
4. Start development

### Bug Reports

When reporting bugs:
1. Check if the issue already exists
2. Provide clear reproduction steps
3. Include browser/environment information
4. Add screenshots if relevant

### Questions?

- Open an issue for technical questions
- Check existing issues and documentation first
- Be patient and respectful in all interactions

## Code of Conduct

- Be respectful and inclusive
- Help others learn and grow
- Focus on constructive feedback
- Maintain a positive environment

Thank you for contributing to RentMeet!