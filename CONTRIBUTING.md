# Contributing to web-playground

## Quick Reference

| Aspect      | Rule                                                  |
| ----------- | ----------------------------------------------------- |
| **Format**  | `type(scope): subject`                                |
| **Subject** | Imperative, <50 chars, lowercase                      |
| **Type**    | `feat` `fix` `docs` `style` `refactor` `test` `chore` |
| **Scope**   | Optional but recommended (e.g., `calculator`, `todo`) |
| **Body**    | Only if change is non-obvious                         |

---

## Commit Types

| Type       | When                                    | Example                                   |
| ---------- | --------------------------------------- | ----------------------------------------- |
| `feat`     | New functionality                       | `feat(calculator): add division operator` |
| `fix`      | Bug resolution                          | `fix(todo): prevent duplicate items`      |
| `docs`     | Documentation only                      | `docs(readme): add troubleshooting`       |
| `style`    | Formatting (Prettier/ESLint)            | `style(demo): apply prettier`             |
| `refactor` | Code reorganization, no behavior change | `refactor(todo): extract validation`      |
| `test`     | Tests only                              | `test(calculator): add unit tests`        |
| `chore`    | Build, deps, tooling                    | `chore(deps): update prettier to 2.8.0`   |

---

## Rules

1. **One commit = one logical change** (atomic)
2. **Imperative mood only** — "add" not "added"
3. **Test before committing** — no broken code
4. **Subject under 50 characters** — use body if needed
5. **No period at end** of subject
6. **Lowercase** subject (except proper nouns)

---

## Examples

### ✅ Good
```

feat(calculator): add square root function
fix(todo): handle empty item names
docs(readme): add API usage examples
chore(git): add .gitignore patterns
style(demo): format calculator.js

```

### ❌ Bad

```

update code
fixed stuff
WIP
add new features to todo app and fix calculator bug
feat: added new buttons (past tense)

```

---

## Workflow

```

# 1. Make changes, test locally

# 2. Review changes

git diff

# 3. Stage

git add .

# 4. Commit

git commit -m "type(scope): subject"

# 5. Verify

git log --oneline -1

# 6. Push

git push origin branch-name

```

---

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Vague subject: "fix: bug" | "fix(calculator): handle division by zero" |
| Multiple changes in one commit | Split into separate commits |
| Committing untested code | Test first, commit after |
| Past tense: "added" | Use imperative: "add" |
| Subject too long (100+ chars) | Keep under 50, use body for details |

---

## When to Add Body

Include body for:
- **Complex changes** — explain rationale
- **Bug fixes** — describe what was wrong
- **Refactoring** — document approach
- **Trade-offs** — mention alternatives considered

Format: Blank line after subject, wrap at 72 chars.

**Example:**
```

feat(calculator): add memory functions (M+, M-, MR, MC)

Previously required manual recalculation or note-taking.
Implementation stores single number in variable with four
standard operations. Persists during session only (design
choice: stateless to avoid storage quota issues).

```

---

## Before Pushing

```

# Verify commits not yet pushed

git log --oneline origin/main..HEAD

# Review all changes

git diff origin/main

# Then push

git push

```

---

## Resources

- [Conventional Commits](https://www.conventionalcommits.org/)
- [Chris Beams — Git Commit Messages](https://chris.beams.io/posts/git-commit/)
- [Pro Git Book](https://git-scm.com/book/en/v2)

---

**TL;DR:** One logical change per commit, `type(scope): subject`, imperative mood, test first, keep subject <50 chars.
