# AI Prototyping Workspace

Rapid HTML/CSS prototyping powered by AI agents (GitLab Duo, Copilot, Claude, Gemini).
Prototypes use **Tailwind CSS**, **Flowbite components**, and shared **design tokens** for consistent styling.

---

## Quick Start

1. **Clone this repo** from GitLab onto your local machine.
2. **Copy the template folder:**
   - Navigate to `/prototypes/template/`
   - Copy the entire folder and rename it to your project name (e.g., `/prototypes/checkout-redesign/`)
3. **Open your new folder** in your editor (VS Code, WebStorm, etc.).
4. **Start prompting your AI agent** with something like:

   > "Using Tailwind, Flowbite, and the design tokens in `/design-system/`, build the initial layout for my checkout redesign."

5. **Preview your work** by opening `index.html` in a browser (no build step required).

---

## What's in the Template

When you copy the template, you get these files:

| File | Purpose |
| ------ | --------- |
| `index.html` | Your main prototype page with Tailwind, Flowbite, and design tokens pre-loaded |
| `flowbite.html` | A reference page with 15 copy-paste Flowbite component snippets |
| `data-example.html` | A working data-driven table loaded from JSON (search, filter, edit, delete) |
| `data.json` | Mock data file -- swap in your own data to power tables and lists |
| `ai-guidelines.md` | Prototype-specific AI rules -- customize for your project |
| `styles.css` | Prototype-specific styles (design token imports are pre-configured) |
| `script.js` | Add any interactive behavior here |

Click the **"Flowbite Snippets"** button in the navbar to browse ready-to-use components, or the **"Data-Driven Example"** card to see a table populated from JSON.

---

## Repository Structure

```text
ai-prototyping/
  README.md                  # This file
  ai-guidelines.md           # Rules for AI agents
  design-system/
    tokens.json              # Design token values (colors, spacing, radii, fonts)
    colors.css               # CSS custom properties for colors
    spacing.css              # CSS custom properties for spacing and radii
    typography.css           # Base typography styles
  prototypes/
    template/                # Starter template
      index.html
      flowbite.html
      data-example.html      # Data-driven table example
      data.json              # Mock data for the example
      ai-guidelines.md       # Prototype-specific AI rules
      styles.css
      script.js
    my-project/              # Your prototype (copy of template)
      index.html
      flowbite.html
      data-example.html
      data.json
      ai-guidelines.md
      styles.css
      script.js
  utils/
    ai-commit-instructions.md  # Instructions for AI agents
```

---

## Technologies

### Tailwind CSS (via CDN)

Utility-first CSS framework. No build step needed -- it's loaded directly in the HTML.

- [Tailwind Docs](https://tailwindcss.com/docs)
- Use classes like `flex`, `grid`, `p-4`, `text-lg`, `bg-blue-700`, etc.

### Flowbite (via CDN)

Pre-built interactive components on top of Tailwind: buttons, modals, dropdowns, tables, navbars, tabs, and more.

- [Flowbite Docs](https://flowbite.com/docs/getting-started/introduction/)
- Components use `data-` attributes for interactivity (modals, dropdowns, tabs, accordion)
- Browse the included `flowbite.html` for copy-paste snippets

### Design Tokens

Shared CSS custom properties in `/design-system/` that keep prototypes consistent:

- **Colors:** `--color-primary`, `--color-secondary`, `--color-danger`, `--color-success`
- **Spacing:** `--spacing-xs` through `--spacing-xl`
- **Radii:** `--radius-sm`, `--radius-md`, `--radius-lg`
- **Typography:** `--font-base`, `--font-sm` through `--font-xl`

Use them in Tailwind with bracket notation: `bg-[var(--color-primary)]` or in regular CSS: `color: var(--color-primary);`

---

## Tips for Working with AI Agents

- **Be specific.** Instead of "build a dashboard", try "build a dashboard with a sidebar nav, a header with a search bar, and a 3-column card grid showing project metrics."
- **Reference this repo.** Tell the agent to check `/design-system/tokens.json` for colors and spacing, and `flowbite.html` for component examples.
- **Iterate.** Start with layout, then refine spacing, then add interactivity. Don't try to get everything perfect in one prompt.
- **Add pages.** Create additional HTML files in your prototype folder (e.g., `settings.html`, `detail.html`) and link between them.
- **Keep it simple.** These are prototypes, not production apps. Prioritize speed and visual fidelity over code quality.

---

## Rules

- Each designer works in their own folder under `/prototypes/`.
- Commit often with clear messages (e.g., "Add settings page layout", "Update card spacing").
- See [ai-guidelines.md](ai-guidelines.md) for the full set of rules your AI agent should follow.

---

## Contributing

Improvements to the shared template, design tokens, and AI guidelines are welcome. Changes to any of the following require a **merge request with approval from at least one other designer**:

- `/prototypes/template/` -- the starter template and Flowbite snippets
- `/design-system/` -- shared design tokens (colors, spacing, typography, radii)
- `ai-guidelines.md` -- global AI agent rules
- `utils/ai-commit-instructions.md` -- AI commit and workflow instructions
- `README.md` -- this file

**How to contribute:**

1. Create a new branch from `main`.
2. Make your changes.
3. Open a merge request and assign at least one other designer as a reviewer.
4. Do not merge until you have at least one approval.

This keeps the shared system stable so everyone's prototypes stay consistent.
