# Design Guidelines

## Git Commit Messages

Commit messages shall follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) rules.

### Format

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Types

- **feat**: A new feature
- **fix**: A bug fix
- **docs**: Documentation only changes
- **style**: Changes that do not affect the meaning of the code (white-space, formatting, etc)
- **refactor**: A code change that neither fixes a bug nor adds a feature
- **perf**: A code change that improves performance
- **test**: Adding missing tests or correcting existing tests
- **build**: Changes that affect the build system or external dependencies
- **ci**: Changes to CI configuration files and scripts
- **chore**: Other changes that don't modify src or test files

### Examples

```
feat: add Pomodoro timer tool
fix: correct timer countdown logic
docs: update README with new tool information
refactor: simplify timer state management
```

### Breaking Changes

Breaking changes should be indicated by:
- Adding `!` after the type/scope: `feat!: remove deprecated API`
- Adding a `BREAKING CHANGE:` footer

Example:
```
feat!: redesign timer interface

BREAKING CHANGE: The timer API has been completely redesigned.
Old timer initialization methods are no longer supported.
```
