# AI Rules & Ecosystem Guidelines

## 🐙 Octopus AI Ecosystem Overview
This repository is part of the **Octopus AI Ecosystem** comprising four core components:
1. **OctopusStudio (`kaleemibnanwar/OctopusStudio`):** Agentic IDE, task DAG orchestrator, and live workspace.
2. **octocut (`kaleemibnanwar/octocut`):** Programmatic video, audio, timeline rendering, and multimodal synthesis engine.
3. **octolimb (`kaleemibnanwar/octolimb`):** OS-level computer use, desktop/browser automation, and vision actuation.
4. **OctopusMCP-Manager (`kaleemibnanwar/OctopusMCP-Manager`):** Model Context Protocol (MCP) tool gateway, registry, and sandbox.

---

## 🛠 Tech Stack Standards
- **Framework & Language:** React 18+ with TypeScript for robust type safety and modern component architecture.
- **Build Tooling:** Vite for lightning-fast development, bundling, and hot module replacement.
- **Routing:** React Router (`react-router-dom`) with route definitions centralized in `src/App.tsx`.
- **Styling:** Tailwind CSS with utility-first classes, custom theming, and CSS variables.
- **UI Component System:** `shadcn/ui` (accessible, customizable primitive components built on Radix UI).
- **Icons:** Lucide React (`lucide-react`) for clean, consistent vector iconography.
- **State Management & Data:** React Hooks and TanStack Query (`@tanstack/react-query`) for asynchronous server state.
- **Forms & Validation:** React Hook Form (`react-hook-form`) combined with Zod for schema validation.
- **Animation & Transitions:** Framer Motion (`framer-motion`) and Tailwind animation utilities.

---

## 📚 Library Usage Rules

| Domain / Purpose | Recommended Library | Usage Rules |
| :--- | :--- | :--- |
| **UI Components** | `shadcn/ui` (Radix UI primitives) | Use pre-built components from `src/components/ui/`. Wrap or compose them in `src/components/`. |
| **Icons** | `lucide-react` | Use Lucide icons exclusively. Do not import external icon packs or write inline SVGs when Lucide icons exist. |
| **Styling & Layout** | Tailwind CSS | Use Tailwind utility classes for all layouts, spacing, colors, and responsive designs. Avoid raw CSS or inline `style`. |
| **Notifications & Toasts** | `sonner` / `shadcn/ui toast` | Use Sonner or the toast provider for notifications across actions. |
| **Routing & Navigation** | `react-router-dom` | Manage navigation using `<Link>`, `useNavigate()`, and standard router hooks in `src/App.tsx`. |
| **Form Handling** | `react-hook-form` + `zod` | Use React Hook Form with Zod schemas (`@hookform/resolvers/zod`). |
| **Data Fetching & Caching** | `@tanstack/react-query` | Use TanStack Query for remote API queries, mutations, cache invalidation, and optimistic updates. |
| **Data Visualization** | `recharts` / `shadcn/ui charts` | Use Recharts via shadcn chart components for dashboards and metric cards. |
| **Date & Time** | `date-fns` | Use `date-fns` for date formatting and manipulation. |
| **Class Merging** | `clsx` + `tailwind-merge` (`cn` utility) | Always use the standard `cn(...)` utility helper when conditionally combining Tailwind classes. |

---

## 📂 Code Organization & Conventions
- **Source Root:** All application code must live inside `src/`.
- **Pages:** Full-page route views reside in `src/pages/`. The primary landing page is `src/pages/Index.tsx`.
- **Components:** Shared or feature components go into `src/components/`, while reusable base UI primitives stay in `src/components/ui/`.
- **Keep Main Page Updated:** Whenever new primary views or interactive widgets are added, ensure they are integrated or linked from `src/pages/Index.tsx` or registered in `src/App.tsx`.
