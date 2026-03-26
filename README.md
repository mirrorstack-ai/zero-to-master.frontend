# Zero to Master: Frontend

Frontend learning roadmap from zero to L3 Software Engineer at [MirrorStack](https://mirrorstack.com).

## Levels

| Level | Title | What you can do |
|-------|-------|----------------|
| L1 | Junior I | Understands fundamentals — HTML/CSS, TypeScript, Git. Can read and modify existing code. |
| L2 | Junior II | Builds features with guidance — React components, Tailwind, writes tests. Needs review on design decisions. |
| L3 | Software Engineer | Works independently — picks up issues, follows patterns, writes clean PRs, debugs own code. |

## Roadmap

### Phase 0 — Setup (Pre-L1)

> Goal: Development environment ready, comfortable with terminal and Git.

- [ ] Install Node.js, pnpm, VS Code
- [ ] Learn terminal basics (cd, ls, mkdir, rm, cat)
- [ ] Learn Git (clone, branch, commit, push, pull, merge)
- [ ] Set up GitHub account, SSH keys
- [ ] **Exercise:** Fork this repo, create a branch, add your name to `students.md`, open a PR

**Resources:**
- [Git Handbook](https://guides.github.com/introduction/git-handbook/)
- [VS Code Getting Started](https://code.visualstudio.com/docs/getstarted/introvideos)

---

### Phase 1 — HTML & CSS (L1)

> Goal: Build static web pages with semantic HTML and modern CSS.

- [ ] HTML elements, forms, tables, semantic tags
- [ ] CSS box model, flexbox, grid
- [ ] Responsive design, media queries
- [ ] CSS variables, transitions, animations
- [ ] **Exercise:** Build a responsive profile card page — `exercises/01-profile-card/`

**Resources:**
- [MDN HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/HTML)
- [MDN CSS Basics](https://developer.mozilla.org/en-US/docs/Learn/CSS)
- [Flexbox Froggy](https://flexboxfroggy.com/)
- [Grid Garden](https://cssgridgarden.com/)

---

### Phase 2 — TypeScript (L1)

> Goal: Write type-safe code. Understand what TypeScript adds over JavaScript.

- [ ] JavaScript basics: variables, functions, arrays, objects, loops
- [ ] Why TypeScript? (JS vs TS comparison)
- [ ] Types: string, number, boolean, arrays, objects
- [ ] Interfaces and type aliases
- [ ] Union types, optional properties, generics basics
- [ ] Modules: import/export
- [ ] **Exercise:** Build a task manager CLI — `exercises/02-typescript/`

**JS vs TS comparison:**

```js
// JavaScript — no safety
function add(a, b) { return a + b; }
add("hello", 5); // "hello5" — silent bug
```

```ts
// TypeScript — catches at compile time
function add(a: number, b: number): number { return a + b; }
add("hello", 5); // ❌ Error: string is not number
```

**Resources:**
- [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/)
- [Total TypeScript Beginners](https://www.totaltypescript.com/tutorials/beginners-typescript)
- [JavaScript.info](https://javascript.info/)

---

### Phase 3 — React + TypeScript (L1 → L2)

> Goal: Build interactive UIs with React. Understand component thinking.

- [ ] JSX and component basics
- [ ] Props and children (with TypeScript interfaces)
- [ ] State with useState, side effects with useEffect
- [ ] Event handling, conditional rendering, lists
- [ ] Custom hooks
- [ ] Component composition patterns
- [ ] **Exercise:** Build a todo app with React — `exercises/03-react-todo/`

**Resources:**
- [React Official Tutorial](https://react.dev/learn)
- [React TypeScript Cheatsheet](https://react-typescript-cheatsheet.netlify.app/)

---

### Phase 4 — Tailwind CSS & Component Patterns (L2)

> Goal: Style components with Tailwind. Understand design system patterns.

- [ ] Utility-first CSS concept
- [ ] Tailwind classes: layout, spacing, colors, typography
- [ ] Responsive design with Tailwind (sm:, md:, lg:)
- [ ] Dark mode with Tailwind
- [ ] Component API design (variants, sizes, colors via props)
- [ ] `cn()` utility (clsx + tailwind-merge)
- [ ] **Exercise:** Rebuild your Phase 1 profile card with React + Tailwind — `exercises/04-tailwind-card/`

**Resources:**
- [Tailwind CSS Docs](https://tailwindcss.com/docs)
- [Tailwind Play](https://play.tailwindcss.com/)

---

### Phase 5 — Testing, Storybook & Workflow (L2 → L3)

> Goal: Write tests, document components in Storybook, follow team workflow.

- [ ] Unit testing with Vitest + Testing Library
- [ ] What to test: logic, user interactions, edge cases
- [ ] Storybook: writing stories, controls, docs
- [ ] Accessibility basics (ARIA, keyboard navigation, screen readers)
- [ ] Git workflow: branch naming, PR conventions, code review
- [ ] **Exercise:** Add tests and stories for your Phase 4 components — `exercises/05-testing/`

**Resources:**
- [Vitest Docs](https://vitest.dev/)
- [Testing Library](https://testing-library.com/docs/react-testing-library/intro)
- [Storybook Tutorials](https://storybook.js.org/tutorials/)
- [web-ui-kit CONTRIBUTING.md](https://github.com/mirrorstack-ai/web-ui-kit/blob/main/CONTRIBUTING.md)

---

### Phase 6 — Graduation (L3)

> Goal: Contribute a real component to the MirrorStack design system.

- [ ] Read [web-ui-kit CONTRIBUTING.md](https://github.com/mirrorstack-ai/web-ui-kit/blob/main/CONTRIBUTING.md)
- [ ] Run `pnpm components list` to see available components
- [ ] Pick an XS issue from the [project board](https://github.com/orgs/mirrorstack-ai/projects/2)
- [ ] Run `pnpm start-issue <number>` to create your branch
- [ ] Port the component following the patterns in Button and Progress
- [ ] Add meta export, stories, and tests
- [ ] Open a PR, address review feedback
- [ ] **Deliverable:** Merged PR to `web-ui-kit`

**Recommended first issues:**
- Icon (WUK-22) — simplest, just a wrapper
- Surface (WUK-28) — simple container
- SectionLabel (WUK-29) — one-line component
- Badge (WUK-16) — small with variants

---

## How it works

1. Work through each phase in order
2. Each exercise is a PR to this repo — your mentor reviews it
3. You can't skip phases, but you can go fast if you already know the material
4. Phase 6 is your graduation — a real contribution to production code

## Timeline

| Phase | Expected duration |
|-------|------------------|
| 0 | 1-2 days |
| 1 | 1 week |
| 2 | 1 week |
| 3 | 2 weeks |
| 4 | 1 week |
| 5 | 1 week |
| 6 | 1 week |
| **Total** | **~7-8 weeks** |

## License

MIT
