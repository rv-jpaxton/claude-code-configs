# Claude Code Configuration

My custom agents and configurations for Claude Code to optimize React/Next.js development workflows.

## Agents

### 1. component-scaffolder
Scaffolds new React components following project patterns (TypeScript, Tailwind, Testing Library).

**Usage:** "Create a new [ComponentName] component"

### 2. test-generator
Generates comprehensive test suites (unit tests, a11y tests, VR test suggestions).

**Usage:** "Generate tests for [ComponentName]"

### 3. pre-commit-checker
Runs comprehensive validation before commits (TypeScript, ESLint, tests, build).

**Usage:** "Check if ready to commit"

### 4. pr-description-generator
Analyzes git diff and generates structured PR descriptions.

**Usage:** "Generate PR description"

## Installation

### Global Setup (all projects)

```bash
# Copy agents to global Claude config
cp -r agents/* ~/.claude/agents/

# Copy global preferences
cp CLAUDE.md ~/.claude/CLAUDE.md
```

### Project-Specific Setup

```bash
# In your project root
mkdir -p .claude/agents
cp agents/* .claude/agents/
```

## Usage

Agents trigger automatically when you use trigger phrases:
- "Create a new Button component" → component-scaffolder
- "Generate tests for Button" → test-generator
- "Am I ready to commit" → pre-commit-checker

Or invoke manually: `/component-scaffolder`

## Customization

Edit agents in `~/.claude/agents/` to customize:
- Model selection (haiku, sonnet, opus)
- Patterns and conventions
- Quality standards
- Output formats

## Project Context

Built for React/Next.js projects with:
- TypeScript
- Tailwind CSS
- Jest + Testing Library
- Playwright (E2E + VR)
- ESLint + Prettier

## License

MIT - Feel free to use and adapt for your workflows
