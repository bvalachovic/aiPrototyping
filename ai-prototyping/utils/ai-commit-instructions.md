# AI Instructions for Working in This Repository

These rules ensure consistent, safe, and predictable prototype generation. AI agents should read this file before making any changes.

---

## 1. Technologies Available

You may use:

- **Tailwind CSS** (loaded via CDN in the template `<head>`)
- **Flowbite** components (CSS and JS loaded via CDN)
- **Design tokens** from `/design-system/` for colors, spacing, typography, and radii
- **HTML, CSS, and minimal JavaScript**

You do **not** need to install anything. Everything works by opening `index.html` in a browser.

---

## 2. Where You Are Allowed to Work

You **must** only modify files inside the active prototype folder, e.g.:

```text
/prototypes/my-project/index.html
/prototypes/my-project/styles.css
/prototypes/my-project/script.js
```

You may create additional HTML files in the prototype folder (e.g., `settings.html`, `detail.html`).

You must **NOT** modify:

- `/prototypes/template/` (the starter template)
- `/design-system/` (shared design tokens)
- `/utils/` (shared instructions)
- `/README.md`

Unless the user explicitly instructs you to.

---

## 3. How to Build Screens

When generating UI:

- Use **Tailwind utility classes** for layout, spacing, and structure.
- Use **Flowbite components** for interactive elements (buttons, modals, dropdowns, tabs, tables, forms).
- Apply **design tokens** using CSS custom properties:

```css
color: var(--color-primary);
padding: var(--spacing-md);
border-radius: var(--radius-md);
```

Or with Tailwind bracket notation:

```html
<div class="bg-[var(--color-primary)] p-[var(--spacing-md)] rounded-[var(--radius-md)]">
```

---

## 4. Available Design Tokens

Reference `/design-system/tokens.json` for the full list. Key values:

| Token | Examples |
| ----- | -------- |
| Colors | `--color-primary`, `--color-secondary`, `--color-danger`, `--color-success`, `--color-muted` |
| Spacing | `--spacing-xs` (4px), `--spacing-sm` (8px), `--spacing-md` (16px), `--spacing-lg` (24px), `--spacing-xl` (32px) |
| Radii | `--radius-sm` (4px), `--radius-md` (8px), `--radius-lg` (12px) |
| Typography | `--font-base` (system-ui), `--font-sm` (14px), `--font-md` (16px), `--font-lg` (20px), `--font-xl` (24px) |

---

## 5. Flowbite Component Reference

The template includes a `flowbite.html` file with 15 copy-paste ready components:

1. Buttons (primary, outline, danger, success, default, disabled)
2. Button Group
3. Badges
4. Alerts (info, danger, success, warning)
5. Cards (simple, with CTA, with list)
6. Form Inputs (text, select, textarea, checkbox, toggle)
7. Table (with status badges and actions)
8. Modal (with header, body, footer)
9. Dropdown
10. Tabs
11. Breadcrumb
12. Pagination
13. Toast (success, error)
14. Accordion
15. Sidebar navigation

Use these snippets as a starting point and customize as needed.

---

## 6. File Structure

Every prototype folder should contain at minimum:

| File | Purpose |
| ----- | -------- |
| `index.html` | Main prototype page |
| `flowbite.html` | Component snippet reference |
| `ai-guidelines.md` | Prototype-specific AI rules (customize per project) |
| `styles.css` | Custom styles (design token imports pre-configured) |
| `script.js` | Custom interactivity |

---

## 7. Prototype-Specific Guidelines

Each prototype folder includes its own `ai-guidelines.md`. **Read this file before making any changes** to a prototype. It contains project-specific rules such as:

- What the prototype is for
- Which pages/screens to build
- Layout preferences and component choices
- Links to reference material (designs, specs, screenshots)

---

## 8. Best Practices

- Use semantic HTML (`<header>`, `<main>`, `<nav>`, `<section>`, `<footer>`, `<button>`, `<form>`).
- Keep JavaScript minimal. Prefer Flowbite's `data-` attribute interactivity.
- Make prototypes responsive using Tailwind breakpoints (`sm:`, `md:`, `lg:`).
- Use clear commit messages that describe what changed and why.
- Do not add external libraries, build tools, or package managers unless the user requests it.
