# AI Rules & Project Guidelines

## Tech Stack
- **Framework & Language:** React 18+ with TypeScript for robust type safety and modern component architecture.
- **Build Tooling:** Vite for lightning-fast development, bundling, and hot module replacement.
- **Routing:** React Router (`react-router-dom`) with all route definitions centralized in `src/App.tsx`.
- **Styling:** Tailwind CSS with utility-first classes, custom theming, and CSS variables for flexible design tokens.
- **UI Component System:** `shadcn/ui` (accessible, customizable primitive components built on Radix UI).
- **Icons:** Lucide React (`lucide-react`) for clean, consistent vector iconography.
- **State Management & Data:** React Hooks (`useState`, `useReducer`, `useContext`) and TanStack Query (`@tanstack/react-query`) for asynchronous server state management.
- **Forms & Validation:** React Hook Form (`react-hook-form`) combined with Zod for schema validation.
- **Animation & Transitions:** Framer Motion (`framer-motion`) and Tailwind animation utilities for micro-interactions and smooth page transitions.

---

## Library Usage Rules

To maintain consistency and avoid redundant packages, follow these strict library choices:

| Domain / Purpose | Recommended Library | Usage Rules |
| :--- | :--- | :--- |
| **UI Components** | `shadcn/ui` (Radix UI primitives) | Use pre-built components from `src/components/ui/`. Do not modify existing UI primitives in place; wrap or compose them into domain-specific components in `src/components/`. |
| **Icons** | `lucide-react` | Use Lucide icons exclusively. Do not import or mix external icon packages (e.g. FontAwesome, React Icons) or write inline SVGs when a Lucide icon exists. |
| **Styling & Layout** | Tailwind CSS | Use Tailwind utility classes for all layouts, spacing, colors, and responsive designs. Avoid raw CSS or inline `style` props unless dynamic values cannot be represented via Tailwind. |
| **Notifications & Toasts** | `sonner` / `shadcn/ui toast` | Use Sonner or the toast provider for toast notifications and user feedback across actions. |
| **Routing & Navigation** | `react-router-dom` | Manage navigation using `<Link>`, `useNavigate()`, and standard router hooks. Keep all top-level routes declared in `src/App.tsx`. |
| **Form Handling** | `react-hook-form` + `zod` | Use React Hook Form with Zod schemas (`@hookform/resolvers/zod`) for form validation, error states, and type-safe submissions. |
| **Data Fetching & Caching** | `@tanstack/react-query` | Use TanStack Query for remote API queries, mutations, cache invalidation, and optimistic updates. |
| **Data Visualization & Charts** | `recharts` / `shadcn/ui charts` | Use Recharts via shadcn chart components for dashboards, metric cards, and data visualizations. |
| **Date & Time Utilities** | `date-fns` | Use `date-fns` for date formatting, parsing, and manipulation. |
| **Class Merging** | `clsx` + `tailwind-merge` (`cn` utility) | Always use the standard `cn(...)` utility helper when conditionally combining Tailwind classes. |

---

## Code Organization & Conventions
- **Source Root:** All application code must live inside `src/`.
- **Pages:** Full-page route views reside in `src/pages/`. The primary landing page is `src/pages/Index.tsx`.
- **Components:** Shared or feature components go into `src/components/`, while reusable base UI primitives stay in `src/components/ui/`.
- **Keep Main Page Updated:** Whenever new primary views or interactive widgets are added, ensure they are integrated or linked from `src/pages/Index.tsx` or registered in `src/App.tsx`.
