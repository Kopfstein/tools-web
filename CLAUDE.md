# CLAUDE.md - AI Assistant Context

## Project Overview

**tools-web** is a collection of productivity tools packaged as static HTML pages. Each tool is self-contained and can run in a web browser without requiring a backend server.

## Current Tools

### Pomodoro Timer
- **Location**: Planned for implementation
- **Specification**: `specs/pomodoro-timer.md`
- **Purpose**: Simple countdown timer for the Pomodoro productivity technique
- **Core Features**:
  - Countdown timer display (minutes:seconds)
  - Quick select buttons (10 min, 25 min)
  - Custom duration input
  - Start/pause controls
  - Gong sound notification when timer expires

## Project Structure

```
tools-web/
├── specs/              # Tool specifications and requirements
│   └── pomodoro-timer.md
├── LICENSE            # Project license
├── README.md          # Project documentation
└── CLAUDE.md          # This file - AI assistant context
```

## Development Guidelines

### Technology Stack
- **HTML/CSS/JavaScript**: All tools should be static pages
- **No Backend Required**: Tools should run entirely in the browser
- **Self-Contained**: Each tool should be a single HTML file (or minimal file set)

### Code Style
- Use modern, vanilla JavaScript (ES6+)
- Keep code simple and readable
- Add comments for complex logic
- Use semantic HTML elements
- Ensure responsive design for mobile and desktop

### File Naming
- Use lowercase with hyphens for filenames: `pomodoro-timer.html`
- Specification files in `specs/` directory: `specs/tool-name.md`

### Implementation Process
1. Review specification in `specs/` directory
2. Create tool as standalone HTML file
3. Test functionality in browser
4. Ensure mobile responsiveness
5. Update README.md with tool information

### Testing Checklist
- [ ] Tool loads without errors
- [ ] All interactive elements work
- [ ] Responsive on mobile and desktop
- [ ] Audio/visual feedback works as expected
- [ ] Accessibility considerations (keyboard navigation, screen readers)

## Branch Naming Convention
- Feature branches: `1-add-Pomodoro-timer`, `2-add-calculator`, etc.
- Bug fixes: `fix-timer-issue`
- Documentation: `docs-update-readme`

## Specifications
All tool specifications are located in the `specs/` directory. Read the specification file before implementing any tool to understand:
- Purpose and use case
- Core features required
- User interface expectations
- Technical requirements

## Notes for AI Assistants
- Always check `specs/` directory for tool requirements before implementation
- Prioritize simplicity and usability
- Each tool should work offline once loaded
- Minimize external dependencies
- Focus on core functionality first, then enhancements
