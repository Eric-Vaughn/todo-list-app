# File Hierarchy
## What is this file?
This file denotes the planned file hierarchy for this project.

As per the goals of this project, I want to practice industry-standard file structures, APIs, & libraries. Having a file structure like this will be good practice.

Note: The below layout is AI generated. Doing this saved me time and numerous Google searches to derive the same outcome: this file hierarchy.
```
todo-app/
├── public/                       # Static assets served directly to the browser
│   ├── favicon.ico
│   └── logo.svg
├── src/
│   ├── app/                      # Next.js App Router (Handles routes, pages, and API)
│   │   ├── layout.tsx            # Global Root Layout (HTML body, theme providers, global CSS)
│   │   │
│   │   ├── (marketing)/          # Route Group for public pages (Homepage, Pricing)
│   │   │   ├── layout.tsx        # PublicLayout (Top marketing nav + footer)
│   │   │   └── page.tsx          # Public landing page (e.g., ://domain.com)
│   │   │
│   │   ├── (auth)/               # Route Group for authentication
│   │   │   ├── layout.tsx        # AuthLayout (Split-screen or centered card framework)
│   │   │   ├── login/page.tsx    # Login view (://domain.comlogin)
│   │   │   └── register/page.tsx # Registration view (://domain.comregister)
│   │   │
│   │   ├── (workspace)/          # Route Group for the main TODO application
│   │   │   ├── layout.tsx        # AppLayout (Persistent sidebar, header, quick-add bar)
│   │   │   ├── dashboard/page.tsx# Main dashboard view (://domain.comdashboard)
│   │   │   ├── inbox/page.tsx    # Inbox task list
│   │   │   ├── today/page.tsx    # Tasks due today
│   │   │   └── projects/[id]/page.tsx # Dynamic project lists (e.g., ://domain.comprojects/work)
│   │   │
│   │   └── api/                  # Backend Serverless API Endpoints
│   │       ├── auth/route.ts     # User authentication endpoints (signup/login sessions)
│   │       └── tasks/route.ts    # Task endpoints (CRUD operations: GET, POST, PUT, DELETE)
│   │
│   ├── components/               # Global Reusable UI Elements (Shared across the app)
│   │   ├── ui/                   # Low-level primitives (Button, Input, Dropdown, Modal)
│   │   ├── TaskItem.tsx          # Single task row/card with checkbox and labels
│   │   └── TaskList.tsx          # Container handling sorting and rendering of task items
│   │
│   ├── hooks/                    # Custom frontend state hooks
│   │   └── useTasks.ts           # React hook managing local UI state, completion, and filters
│   │
│   ├── lib/                      # Backend initializations and database clients
│   │   └── db.ts                 # Database connector (e.g., Prisma or MongoDB client)
│   │
│   └── utils/                    # Pure JavaScript helper functions
│       └── dateHelpers.ts        # Formatting functions for task due dates (e.g., "Due Tomorrow")
│
├── .env.local                    # Database credentials and secret keys (never commit to GitHub)
├── package.json                  # Scripts and npm dependencies
└── tsconfig.json                 # TypeScript compiler configuration

```