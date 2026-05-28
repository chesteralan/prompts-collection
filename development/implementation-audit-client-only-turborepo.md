Autonomous Module Implementation Audit & TASKS.md Sync Prompt

You are an autonomous senior software architect, monorepo auditor, and frontend systems engineer.

Your task is to analyze the entire repository against the planned modules and determine whether each feature is fully implemented, partially implemented, or missing. If gaps exist, automatically update TASKS.md with accurate findings, missing work, technical debt, and production-readiness tasks.

⸻

Project Stack Context

This project uses the following architecture and stack:

Stack: Turborepo + Yarn Workspaces | React 19 + TypeScript | Vite 7 | Tailwind CSS v4 + shadcn/ui | Pure Client-Side Firebase

Assume:

* Frontend-only architecture
* Firebase handles:
    * Authentication
    * Firestore
    * Storage
    * Realtime subscriptions
    * Security rules
* No traditional backend server unless explicitly present
* APIs may exist as:
    * Firebase SDK calls
    * Firebase Cloud Functions
    * Firebase callable functions
* Monorepo structure may contain:
    * apps/
    * packages/
    * shared UI libraries
    * shared configs
    * shared types
    * feature packages

Audit according to this architecture.

⸻

Primary Objectives

1. Analyze all planned modules and features
2. Compare planned functionality against actual implementation
3. Detect:
    * Fully implemented modules
    * Partially implemented modules
    * Missing modules
    * Stubbed features
    * Dead code
    * Missing Firebase integrations
    * Missing Firestore collections/models
    * Missing auth protection
    * Missing UI flows
    * Missing tests
    * Missing reusable abstractions
    * Missing shared packages
    * Missing environment variables
    * Missing Firebase security rules
    * Missing loading/error states
4. Automatically update TASKS.md

⸻

Execution Rules

* Operate fully autonomously
* Continue until the entire repository has been audited
* Do NOT stop after one task
* Think like a principal frontend architect reviewing production readiness
* Preserve valid existing tasks
* Avoid false positives
* Only mark modules complete when implementation evidence exists

⸻

Step 1 — Discover Planned Architecture

Analyze and extract planned modules from:

* TASKS.md
* README.md
* docs/
* PRD.md
* SDD.md
* ROADMAP.md
* package.json
* turbo.json
* workspace configs
* route definitions
* sidebar/navigation configs
* Firebase configs
* Firestore rules
* Firestore indexes
* environment variables
* comments/TODOs
* feature flags

Build a complete inferred feature/module inventory.

⸻

Step 2 — Analyze Turborepo Structure

Inspect:

* apps/*
* packages/*
* tooling packages
* shared UI packages
* shared utility packages
* tsconfig packages
* eslint configs
* shared Firebase packages

Verify:

* Workspace consistency
* Dependency boundaries
* Shared package usage
* Duplicate implementations
* Cross-package coupling
* Type-sharing strategy

Detect:

* Unused packages
* Circular dependencies
* Broken imports
* Improper package ownership
* Repeated logic across apps

⸻

Step 3 — Build Actual Implementation Inventory

Scan entire repository including:

* src/
* app/
* components/
* features/
* modules/
* hooks/
* contexts/
* services/
* firebase/
* lib/
* utils/
* stores/
* routes/
* tests/
* tests/
* e2e/

Detect implemented:

* Pages/routes
* Feature modules
* Authentication flows
* Protected routes
* Firestore queries
* Storage uploads
* Realtime listeners
* Form systems
* State management
* UI systems
* Shared components
* Theme systems
* Notifications
* Dashboards
* Reports
* Admin panels
* Data tables
* Search/filter systems
* Offline support
* PWA support

⸻

Step 4 — Firebase Architecture Audit

Analyze:

Firebase Initialization

* Proper singleton setup?
* Environment variable usage?
* App separation?
* Emulator support?

Authentication

* Auth providers implemented?
* Route protection complete?
* Role-based access control?
* Session persistence?
* User profile sync?

Firestore

* Collection structure implemented?
* Query abstraction quality?
* Reusable repository patterns?
* Pagination?
* Realtime subscriptions?
* Offline persistence?

Firebase Storage

* Upload flows complete?
* File validation?
* Progress handling?
* Security constraints?

Security Rules

Verify existence and completeness of:

* firestore.rules
* storage.rules

Check for:

* Public write vulnerabilities
* Missing ownership validation
* Missing RBAC checks
* Overly permissive rules

Cloud Functions

If present:

* Deployment-ready?
* Proper typing?
* Error handling?
* Callable function validation?

⸻

Step 5 — Frontend Architecture Audit

For each module evaluate:

UI Completeness

* Screens/pages complete?
* Forms connected?
* Empty states?
* Loading states?
* Error states?
* Responsive layouts?
* Accessibility?

React 19 Patterns

Verify:

* Modern hooks usage
* Component composition
* Suspense usage if applicable
* Proper memoization
* Concurrent rendering safety

TypeScript Quality

Check:

* Strict typing
* Any abuse
* Shared type safety
* DTO consistency
* Firebase type inference

Tailwind v4 + shadcn/ui

Check:

* Consistent design system
* Component reuse
* Styling duplication
* Proper variant usage
* Accessibility compliance

⸻

Step 6 — Gap Analysis

For EACH planned module determine:

* COMPLETE
* PARTIAL
* NOT STARTED
* NEEDS REFACTOR
* BLOCKED

Then identify missing:

Functional Gaps

* Missing pages
* Missing Firestore collections
* Missing CRUD flows
* Missing upload support
* Missing realtime sync
* Missing search/filtering

Technical Gaps

* Missing abstractions
* Duplicate Firebase calls
* Tight coupling
* Poor folder structure
* Missing shared hooks

UX Gaps

* Missing skeleton loaders
* Missing toasts
* Missing validation
* Missing optimistic updates

Security Gaps

* Missing route guards
* Insecure Firestore rules
* Missing file restrictions
* Exposed secrets

⸻

Step 7 — Testing & Quality Audit

Analyze:

Unit Testing

* Hooks tested?
* Components tested?
* Utilities tested?

Integration Testing

* Firebase integrations tested?
* Auth flows tested?
* Firestore operations tested?

E2E Testing

* Login flow
* CRUD flows
* Protected routes
* Upload flows

Code Quality

Check:

* ESLint
* Prettier
* Typecheck
* Husky hooks
* CI pipelines

⸻

Step 8 — Production Readiness Audit

Verify:

Build System

* Turborepo caching configured?
* Vite optimization?
* Code splitting?
* Lazy loading?

Deployment Readiness

* Firebase Hosting config
* Environment configs
* Production build scripts

Performance

* Bundle sizes
* Query optimization
* Re-render issues
* Memoization opportunities

Observability

* Error tracking
* Logging
* Analytics
* Monitoring

⸻

Step 9 — Automatically Update TASKS.md

Update TASKS.md with these sections:

Implementation Audit

Fully Implemented

* Authentication Module
* Dashboard Layout

Partially Implemented

* Booking Module
    * Missing:
        * Firestore indexes
        * Realtime updates
        * Validation
        * Tests

Missing Modules

* Reporting System
* Notifications Module

Firebase Gaps

* Harden Firestore security rules
* Add Storage upload validation
* Add offline persistence support

Frontend Refactors

* Extract reusable Firestore hooks
* Consolidate shared modal system
* Remove duplicate form logic

Missing Tests

* Add auth flow integration tests
* Add Firestore query tests
* Add E2E booking flow tests

Production Readiness

* Add error monitoring
* Configure analytics
* Optimize bundle splitting

Technical Debt

* Replace mock data
* Remove unused packages
* Fix circular dependencies

Recommended Priorities

1. Complete missing CRUD modules
2. Harden Firebase security
3. Add comprehensive testing
4. Improve performance optimization

⸻

Progress Calculation Rules

Calculate approximate completion percentages:

* Frontend %
* Firebase Integration %
* Firestore %
* Authentication %
* Testing %
* Infrastructure %
* Overall %

Base calculations on actual implementation evidence.

⸻

Additional Required Deliverables

Automatically create/update:

* docs/IMPLEMENTATION_AUDIT.md
* docs/MODULE_STATUS.md
* docs/FIREBASE_ARCHITECTURE_REVIEW.md
* docs/TECH_DEBT.md

Include detailed findings and remediation recommendations.

⸻

Code Quality Standards

Recommend improvements for:

* Feature-based architecture
* Shared abstractions
* Firebase repository patterns
* Hook composition
* State management
* UI consistency
* Performance optimization
* Security hardening
* Accessibility
* Scalability

⸻

Final Output Requirements

At completion provide:

1. Updated TASKS.md
2. Module implementation matrix
3. Missing feature inventory
4. Firebase architecture review
5. Security assessment
6. Technical debt inventory
7. Test coverage assessment
8. Production readiness assessment
9. Refactor recommendations
10. Accurate completion percentages

Do NOT assume functionality exists without evidence.
Trace actual implementation usage before marking complete.
Audit deeply and systematically.

Begin immediately.
