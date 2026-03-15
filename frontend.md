# 🎨 Frontend

> Everything the user sees and interacts with. The art of turning data into experiences.

---

## 🧱 Core Web

| Tech | What it's for | Priority |
|------|--------------|----------|
| **HTML5** | Content structure. Semantics matter (SEO, accessibility, screen readers) | Must-know |
| **CSS3** | Flexbox, Grid, custom properties, animations, media queries | Must-know |
| **JavaScript ES6+** | Async/await, modules, destructuring, spread, optional chaining | Must-know |
| **TypeScript** | Static types for JS — fewer runtime bugs, better IDE experience | Must-know |
| **Web APIs** | Fetch, WebSocket, localStorage, IndexedDB, Service Workers, Intersection Observer | Important |
| **Accessibility (A11y)** | ARIA roles, keyboard navigation, color contrast, screen reader support | Must-know |
| **SEO basics** | Meta tags, structured data, canonical URLs, Core Web Vitals | Important |

---

## ⚛️ UI Frameworks

| Framework | What it's for | When to use |
|-----------|--------------|-------------|
| **React** | Component-based UI library, hooks, virtual DOM | Complex apps, largest ecosystem |
| **Next.js** | React + SSR/SSG/ISR + file routing + API routes + middleware | Full-stack apps, SEO critical |
| **Vue 3** | Progressive framework, Composition API, reactivity system | Medium projects, gentle curve |
| **Nuxt** | Vue equivalent of Next.js — SSR, SSG, full-stack | Vue projects needing SSR/SSG |
| **Svelte** | Compiles to vanilla JS at build time — no virtual DOM | Lightweight, performance-sensitive |
| **Astro** | Islands architecture — partial hydration, multi-framework | Content-heavy sites, blogs, docs |
| **Remix** | Full-stack React with nested loaders + actions | Data-heavy apps, progressive enhancement |
| **SolidJS** | Reactive primitives, no virtual DOM, very performant | Performance-critical SPAs |

---

## 🎨 CSS & Styling

| Tech | What it's for |
|------|--------------|
| **Tailwind CSS** | Utility-first. Design in markup, rapid prototyping, consistent tokens |
| **CSS Modules** | Component-scoped styles — no global namespace collisions |
| **Styled Components** | CSS-in-JS for React — co-locate styles with components |
| **Sass/SCSS** | Variables, mixins, nesting, functions |
| **Shadcn/UI** | Accessible copy-paste components built on Radix UI |
| **Radix UI** | Unstyled, WAI-ARIA compliant primitives |
| **Framer Motion** | Production-ready animation library for React |

---

## 🔄 State Management & Data Fetching

| Tech | What it's for | Use case |
|------|--------------|----------|
| **TanStack Query** | Server state: caching, background sync, pagination, optimistic updates | API-heavy apps |
| **Zustand** | Minimalist global client state — simple API, no boilerplate | Most React apps |
| **Redux Toolkit** | Scalable opinionated global state with DevTools | Large teams, complex state |
| **Jotai** | Atomic state model — granular, bottom-up | Complex derived state |
| **SWR** | Stale-while-revalidate data fetching by Vercel | Simple data fetching |
| **Valtio** | Proxy-based reactive state — mutate directly | When mutation feels natural |
| **Context API** | Built-in React — good for low-frequency updates (theme, locale) | Simple global state |

---

## ⚡ Build Tools & Runtimes

| Tech | What it's for |
|------|--------------|
| **Vite** | Ultra-fast dev server using native ESM + optimized production bundler |
| **Bun** | Fast JS runtime + package manager + bundler + test runner in one |
| **Webpack** | Fully configurable bundler — extensive plugin ecosystem (legacy) |
| **esbuild** | Go-based compiler, extremely fast — powers Vite internally |
| **Turbopack** | Rust-based Webpack successor by Vercel (Next.js default) |
| **Rollup** | Library bundler — optimal tree-shaking for packages |
| **pnpm** | Faster npm using hard links and content-addressable storage |

---

## 🧪 Testing

| Tech | What it's for |
|------|--------------|
| **Vitest** | Jest-compatible unit testing built for Vite — fast, native ESM |
| **Testing Library** | Test components how real users interact (accessible queries) |
| **Playwright** | E2E testing in Chromium, Firefox, WebKit — cross-browser |
| **Cypress** | E2E with visual UI, time-travel debugging, network stubbing |
| **Jest** | Classic unit + integration testing runner with snapshot support |
| **Storybook** | Component development in isolation + visual regression testing |
| **MSW** | Mock Service Worker — intercept network requests in tests and dev |

---

## ⚡ Performance

| Concept | What it means |
|---------|--------------|
| **Core Web Vitals** | LCP (loading), INP (interactivity), CLS (visual stability) — Google signals |
| **Lazy loading** | Load components/images only when needed — React.lazy, Intersection Observer |
| **Code splitting** | Split JS bundle by route — reduce initial load time |
| **Tree shaking** | Remove unused code at build time via ES modules static analysis |
| **Image optimization** | WebP/AVIF formats, responsive srcset, lazy loading, CDN delivery |
| **Prefetching** | Load next routes/resources before user navigates |
| **Bundle analysis** | webpack-bundle-analyzer, vite-plugin-inspect — find bloat |
| **Lighthouse** | Automated audits: performance, accessibility, SEO, best practices |
| **Web Workers** | Offload CPU-intensive work from the main thread |

---

## 🗺️ Suggested Roadmap

```
HTML/CSS/JS basics
    → TypeScript
    → React (hooks, composition patterns)
    → Next.js (SSR/SSG, App Router)
    → TanStack Query + Zustand
    → Testing (Vitest + Playwright)
    → Performance & Accessibility
    → Advanced patterns (streaming, islands, RSC)
```
