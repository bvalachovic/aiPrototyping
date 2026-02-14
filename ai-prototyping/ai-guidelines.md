# AI Agent Guidelines

These rules apply to any AI agent (GitLab Duo, Copilot, Claude, Gemini, etc.) generating or modifying prototypes in this repository.

---

## 1. Work only in your prototype folder

- Modify files **only** inside the active prototype folder (e.g., `/prototypes/my-project/`).
- **Never** modify `/prototypes/template/`, `/design-system/`, `/utils/`, or `README.md` unless the user explicitly asks you to.

## 2. Use Tailwind CSS for layout and styling

- Use Tailwind utility classes (`flex`, `grid`, `p-4`, `text-sm`, `bg-white`, etc.) for all layout, spacing, and visual styling.
- Avoid writing custom CSS unless Tailwind cannot handle the requirement.
- Use bracket notation for design tokens: `bg-[var(--color-primary)]`, `p-[var(--spacing-md)]`.

## 3. Use Flowbite for interactive components

- Use Flowbite components for buttons, modals, dropdowns, tabs, tables, navbars, accordions, toasts, and forms.
- Flowbite CSS and JS are already loaded via CDN in the template -- no additional setup needed.
- Reference `/prototypes/template/flowbite.html` for copy-paste ready snippets.
- Flowbite interactivity uses `data-` attributes (e.g., `data-modal-toggle`, `data-dropdown-toggle`, `data-tabs-toggle`).

## 4. Apply design tokens for consistency

- Colors, spacing, radii, and typography are defined as CSS custom properties in `/design-system/`.
- Reference `/design-system/tokens.json` for the full list of available values.
- Use CSS variables in your styles: `color: var(--color-primary);`, `padding: var(--spacing-md);`.

## 5. Use semantic HTML

- Prefer semantic elements: `<header>`, `<main>`, `<section>`, `<nav>`, `<aside>`, `<footer>`, `<button>`, `<form>`.
- Use heading hierarchy correctly (`h1` > `h2` > `h3`).
- Add `aria-label`, `role`, and other accessibility attributes where appropriate.

## 6. Read the prototype-specific guidelines

Each prototype folder includes its own `ai-guidelines.md` with project-specific rules (layout preferences, pages to build, components to favor, etc.). **Read this file first** before making changes to a prototype.

## 7. Keep prototypes self-contained

Each prototype folder should contain:

- `index.html` -- main page
- `flowbite.html` -- component reference (copied from template)
- `ai-guidelines.md` -- prototype-specific AI rules
- `styles.css` -- prototype-specific styles
- `script.js` -- prototype-specific interactivity
- Additional `.html` files as needed for multi-page prototypes

## 8. Keep it simple

- These are prototypes, not production code. Prioritize speed and visual fidelity.
- Minimize custom JavaScript. Use Flowbite's built-in interactivity where possible.
- Avoid installing packages, build tools, or frameworks beyond what's in the template.

## 9. Commit messages

Use clear, descriptive commit messages:

- "Add dashboard layout with sidebar and cards"
- "Update settings form with toggle inputs"
- "Fix modal close button alignment"
- "Add detail page linked from table rows"
