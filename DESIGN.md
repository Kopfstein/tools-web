# Project Software Design Guidelines

## Design Philosophy

The tools in this project prioritize simplicity and shall work without build steps. All tools are designed to work as one-file static web pages.

## Architecture

- **One single html file per tool**, including html, css, and javascript.
- **Responsive design**, mobile first.
- No build steps, tools should work when opened in browser.
- Use localStorage for persistence.
- Support modern browsers Chrome, Firefox, Edge, no support for old browsers such as IE11 required.

## User Interface and Visual Design

- Aim for clear and simple UI.
- Add keyboard navigation.
- Sufficient color contrast (WCAG AA).
- Implement light & dark mode based on system.

## Coding Style

- Keep code simple, human readable, and use small functions.
- Add comments to enhance readability.
- Use consistent indentation of 4 spaces.
- Use semantic HTML 5 elements.

## Allowed

- Standard HTML 5.
- Standard JavaScript ES6.
- Tachyons CSS for styling, loaded via CDN.
- Vega-lite for visualization of data, loaded via CDN.

## Prohibited

- React, Vue, or any other framework requiring build steps.
- Node.js dependencies or npm packages (CDN only).
- Typescript or other transpiled languages.

## Preferred Libraries

### Tachyons CSS

Use Tachyons for utility-first CSS styling:

```html
<link rel="stylesheet" href="https://unpkg.com/tachyons@4.12.0/css/tachyons.min.css">
```

**Why Tachyons:**
- Pure CSS, no JavaScript required (~14KB minified + gzipped)
- Designed specifically for CDN use
- Fast loading with no runtime compilation
- Works offline once cached
- Utility-first approach similar to Tailwind but more lightweight

**Custom styles:** For features not available in Tachyons (e.g., specific colors, dark mode utilities), add custom CSS in a `<style>` tag.

---

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
