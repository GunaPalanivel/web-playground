# Web-Playground 🎮

A enterprise-grade learning project demonstrating professional full-stack development practices, from dev environment setup to production-ready code patterns.

## 📋 Sessions & Deliverables

### Session 1: VS Code & Extensions Fundamentals

**Objective:** Configure professional development environment

**Deliverables:**

- ✅ `.vscode/settings.json` with Prettier configuration
- ✅ `.vscode/extensions.json` for team recommendations
- ✅ `EXTENSIONS.md` documenting each extension
- ✅ `.prettierrc` with code style standards
- ✅ `.eslintrc.json` for code quality

**Key Concepts:** IDE configuration, formatting standards, linting setup

### Session 2: Git Workflow & Local Development

**Objective:** Master professional Git practices

**Deliverables:**

- ✅ Initialized repo with meaningful commits
- ✅ `.gitignore` with comprehensive exclusions
- ✅ `CONTRIBUTING.md` with commit conventions
- ✅ Configured user.name and user.email
- ✅ Default branch set to main

**Key Concepts:** Version control, atomic commits, meaningful messages, collaborative workflows

## 🚀 Quick Start

### Prerequisites

- Git (v2.28+) — [Download](https://git-scm.com/downloads)
- VS Code Insiders — [Download](https://code.visualstudio.com/insiders/)
- Node.js (optional, for advanced features) — [Download](https://nodejs.org)

### Setup Instructions (3 Steps)

**Step 1: Clone/Initialize Repository**

```
cd web-playground
git config --local user.name "Your Name"
git config --local user.email "your@email.com"
```

**Step 2: Install VS Code Extensions**

- Open VS Code
- Press `Ctrl+Shift+X` (Extensions)
- Extensions automatically recommended (or install manually: Prettier, Live Server, ESLint)

**Step 3: Launch Development Server**

- Right-click any `.html` file
- Select "Open with Live Server"
- Browser opens automatically with live reload enabled

✅ **You're ready to code!**

## 📝 Commit Convention

**Format:** `type(scope): subject`

**Example:**

```
feat(vscode): configure prettier with code style standards
fix(calculator): resolve division by zero error
docs(readme): add architecture decision section
style(demos): format all files with prettier
chore(git): add .gitignore exclusions
```

**Types:**

- `feat` — New feature or functionality
- `fix` — Bug fix or correction
- `docs` — Documentation changes only
- `style` — Code formatting (prettier, eslint fixes)
- `refactor` — Code restructuring without behavior change
- `test` — Adding or updating tests
- `chore` — Build, dependencies, tooling (non-code changes)

**Rules:**

- ✅ Imperative mood: "add" not "added" or "adds"
- ✅ Lowercase subject
- ✅ No period at end
- ✅ Maximum 50 characters for subject
- ✅ Each commit is atomic (one logical change)

**Full Message Example:**

```
feat(vscode): configure prettier with code style standards

Set quote style to single quotes
Configure trailing commas for ES5 compatibility
Define tab width as 2 spaces
Add format-on-save for consistency

These standards ensure team-wide code consistency and reduce
merge conflicts caused by formatting differences.
```

**Reference:** [Conventional Commits](https://www.conventionalcommits.org/)

## 🔄 Git Workflow

### Branch Strategy

| Branch Type | Purpose           | Naming                     | Lifespan           |
| ----------- | ----------------- | -------------------------- | ------------------ |
| `main`      | Production-ready  | —                          | Permanent          |
| `feature/*` | Session/task work | `feature/descriptive-name` | Delete after merge |
| `hotfix/*`  | Urgent fixes      | `hotfix/issue-name`        | Delete after merge |

**Example:**

```
main (production)
├── feature/vscode-config ← merged
├── feature/git-workflow ← current
└── feature/calculator-demo ← planned
```

### Commit Frequency

| Scenario    | Frequency   | Pattern                           |
| ----------- | ----------- | --------------------------------- |
| Small fix   | 1 commit    | `fix(scope): specific change`     |
| Feature     | 1-3 commits | Break into logical steps          |
| Refactoring | 1 commit    | `refactor(scope): extract module` |

**Do's:**

- ✅ Commit when logical unit is complete
- ✅ Commit at least once per session
- ✅ Commit before taking breaks

**Don'ts:**

- ❌ Commit broken code
- ❌ Mix multiple features in one commit
- ❌ Save everything in one EOD commit

### Merge Strategy

**Use No-FF (Preserve History):**

```
git checkout main
git merge feature/git-workflow --no-ff -m "feat(session-2): complete git workflow setup"
git push origin main
```

**Benefits:** Shows branch history, easy to revert, professional standard.

### Pre-Push Checklist

```
# 1. Test locally (no errors in browser/console)
# 2. Verify ESLint passes (no red underlines)
# 3. Save files (Prettier auto-formats)
# 4. Check what's being pushed
git diff origin/main

# 5. Push
git push origin feature/git-workflow
```

### Undo Reference

| Situation                       | Command                       |
| ------------------------------- | ----------------------------- |
| Undo last commit (not pushed)   | `git reset --hard HEAD~1`     |
| Undo last commit (keep changes) | `git reset --soft HEAD~1`     |
| Undo pushed commit              | `git revert <commit-hash>`    |
| Save WIP temporarily            | `git stash` / `git stash pop` |

---

## 🔧 VS Code & Extensions

### Installed Extensions

| #   | Extension   | Publisher   | Purpose                                                     |
| --- | ----------- | ----------- | ----------------------------------------------------------- |
| 1   | Prettier    | esbenp      | Automatic code formatting for JavaScript, HTML, CSS, JSON   |
| 2   | Live Server | Ritwick Dey | Local development server with live reload on file changes   |
| 3   | ESLint      | Dirk Bäumer | JavaScript linting to catch errors and enforce code quality |

### Extension Details & Configuration

**Prettier — Code Formatter**

- **Purpose:** Enforces consistent code style automatically
- **How It Works:** Formats code on save (configured in `.vscode/settings.json`)
- **Usage:** Write code however you want → Prettier auto-formats on Ctrl+S
- **Config File:** `.prettierrc` defines style rules (quotes, indentation, etc.)
- **Team Benefit:** Eliminates style discussions in code reviews

**Live Server**

- **Purpose:** Run local development server with auto-refresh
- **How It Works:** Detects file changes → Automatically reloads browser
- **Usage:** Right-click `.html` file → "Open with Live Server"
- **Config:** Configured to use Chrome browser by default
- **Team Benefit:** Instant feedback loop, faster development iteration

**ESLint**

- **Purpose:** Find and fix problems in JavaScript code
- **How It Works:** Analyzes code against configured rules, shows warnings/errors
- **Usage:** Write JavaScript → Red squiggles show issues → Fix them
- **Config File:** `.eslintrc.json` defines which rules to enforce
- **Team Benefit:** Catches bugs early, enforces best practices

### Setup Verification

```
# Check Prettier config
cat .prettierrc

# Check ESLint config
cat .eslintrc.json

# Verify VS Code settings
cat .vscode/settings.json | grep defaultFormatter
```

## 🐛 Troubleshooting

### Q: Live Server not working

```
# Solution 1: Reload VS Code (Ctrl+R)
# Solution 2: Reinstall Live Server extension
# Solution 3: Check .html file is in project root or demos/ folder
```

### Q: Prettier not formatting on save

Check `settings.json` has this line:

```
"editor.formatOnSave": true
```

If not, verify `.vscode/settings.json` exists and is valid JSON.

### Q: Git commits failing

```
# Verify git config
git config --global user.name     # Should show your name
git config --global user.email    # Should show your email

# If empty, run:
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

## 📚 Learning Resources

### Git & Version Control

- [Pro Git — Git Basics](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials)
- [Conventional Commits](https://www.conventionalcommits.org/)

### VS Code & Development Environment

- [VS Code Tips and Tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)
- [VS Code Extension Marketplace](https://code.visualstudio.com/docs/editor/extension-marketplace)
- [Keyboard Shortcuts — Windows](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows)

## 📊 Progress Tracking

- [x] Session 1: VS Code & Extensions
- [x] Session 2: Git Workflow
- [ ] Session 3: JavaScript Fundamentals (Planned)
- [ ] Session 4: DOM Manipulation (Planned)
- [ ] Session 5: API Integration (Planned)
