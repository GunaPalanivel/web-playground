# VS Code Extensions Guide

Recommended extensions for the web-playground project. These are automatically suggested when you open the project in VS Code.

## Quick Start

**Option 1: Automatic**
- VS Code shows a notification bell with recommended extensions
- Click the notification and install all three

**Option 2: Manual**
- Press `Ctrl+Shift+X` (Extensions panel)
- Search for each extension by name below
- Click Install

---

## Recommended Extensions

### 1. Prettier — Code Formatter

| Property | Value |
|----------|-------|
| Publisher | Prettier |
| ID | `esbenp.prettier-vscode` |
| Purpose | Auto-format code on save |

**What it does:** Automatically formats code to match project style. Saves time and eliminates formatting debates.

**How to use:**
- Write code normally
- Press `Ctrl+S` to save
- Prettier auto-formats your code

**Configuration:**
- Config file: `.prettierrc` (already set up)
- VS Code settings: `.vscode/settings.json` (has `formatOnSave: true`)

**Before & After:**

```
// Before
function hello( name,age ){
return `Hello ${name}, you are ${age}`;
}

// After (auto-formatted)
function hello(name, age) {
  return `Hello ${name}, you are ${age}`;
}
```

**Terminal commands:**
```
npx prettier --write src/          # Format directory
npx prettier --check src/          # Check without changing
npx prettier --diff src/           # See what would change
```

---

### 2. Live Server

| Property | Value |
|----------|-------|
| Publisher | Ritwick Dey |
| ID | `ritwickdey.LiveServer` |
| Purpose | Local dev server with auto-refresh |

**What it does:** Runs your HTML locally and auto-refreshes the browser when you save files.

**How to use:**
1. Right-click any `.html` file
2. Select **"Open with Live Server"**
3. Browser opens automatically (Chrome by default)
4. Every file save triggers a browser refresh

**Without Live Server:**
- Edit HTML → Save → Alt+Tab to browser → Press F5 → See changes
- Slow and repetitive

**With Live Server:**
- Edit HTML → Save → Changes appear instantly
- Stay in your editor, see changes live

**Configuration:**
- Port: `5500` (default)
- Browser: Chrome (configured in `.vscode/settings.json`)
- Auto-refresh: Enabled for all file changes

**Quick tips:**
- Click "Go Live" button in VS Code status bar (bottom-right)
- Works with HTML, CSS, JavaScript, and assets
- Perfect for demos in `demos/` folder

---

### 3. ESLint

| Property | Value |
|----------|-------|
| Publisher | Dirk Bäumer |
| ID | `dbaeumer.vscode-eslint` |
| Purpose | Real-time JavaScript error detection |

**What it does:** Catches JavaScript errors as you type. Shows warnings/errors before you run the code.

**How to use:**
- Write JavaScript
- Red squiggles appear under problems
- Hover to see the issue
- Press `Ctrl+.` (Quick Fix) to auto-correct

**Common errors it catches:**

| Error | Example | Fix |
|-------|---------|-----|
| Undefined variable | `console.log(naem);` | Rename to `name` |
| Using `var` | `var x = 5;` | Use `let` or `const` |
| Loose equality | `if (x == 5)` | Use `===` |
| Unused variables | `var unused = 5;` | Remove or use it |
| Missing semicolons | `const x = 5` | Add `;` |

**Configuration:**
- Config file: `.eslintrc.json` (defines which rules apply)
- Auto-fix on save: Enabled in `.vscode/settings.json`

**Keyboard shortcuts:**
```
Ctrl+.              → Quick fix for current error
Ctrl+Shift+P        → ESLint: Fix all auto-fixable problems
```

**Disable for specific line:**
```
// eslint-disable-next-line no-var
var x = 5;  // Rule ignored just for this line
```

---

## Extension Comparison

| Extension | When to Use | Trigger |
|-----------|------------|---------|
| **Prettier** | After every edit | Ctrl+S (automatic) |
| **Live Server** | Testing HTML/CSS | Right-click `.html` → Open with Live Server |
| **ESLint** | Writing JavaScript | Real-time as you type |

---

## Troubleshooting

### Prettier Not Formatting on Save

**Problem:** Code doesn't auto-format when you press `Ctrl+S`

**Solution:**
1. Check `.vscode/settings.json` has: `"editor.formatOnSave": true`
2. Reload VS Code: `Ctrl+R`
3. Reinstall Prettier: Extensions → Uninstall → Reinstall

### Live Server Browser Doesn't Open

**Problem:** "Go Live" clicked but browser stays closed

**Solution:**
1. Verify file is `.html` (not `.txt` or other type)
2. Check Chrome is installed
3. View output: VS Code → Output → Live Server

### ESLint Shows No Errors

**Problem:** ESLint not detecting issues

**Solution:**
1. Verify `.eslintrc.json` exists in project root
2. Reload VS Code: `Ctrl+R`
3. Check status: `Ctrl+Shift+P` → "ESLint: Show Output"

---

## Resources

- [Prettier Documentation](https://prettier.io/)
- [ESLint Documentation](https://eslint.org/)
- [VS Code Tips & Tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)
- [Live Server GitHub](https://github.com/ritwickdey/vscode-live-server-plus-plus)
