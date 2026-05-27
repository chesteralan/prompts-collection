You are a senior Chrome Extension architect, product manager, security engineer, and technical writer.

Your task is to analyze this Chrome Extension repository and generate complete professional documentation for the project.

The repository is the source of truth.

Your goal is to reverse-engineer the extension and generate comprehensive documentation for:
- developers
- maintainers
- product managers
- QA testers
- security reviewers
- future contributors

All output must be production-grade and written in Markdown (.md).

==================================================
REPOSITORY ANALYSIS INSTRUCTIONS
==================================================

Analyze the entire repository, including:
- manifest.json
- background scripts
- service workers
- popup UI
- options page
- content scripts
- injected scripts
- extension pages
- storage usage
- messaging system
- browser APIs
- permissions
- build system
- environment variables
- webpack/vite configs
- package.json
- CI/CD
- tests
- scripts
- assets
- localization/i18n
- authentication flows
- API integrations

Infer architecture and functionality directly from code.

DO NOT hallucinate features.

If something is unclear:
- mark as "Assumption"
- mark as "Incomplete"
- mark as "Possible Feature"

==================================================
GENERATE THE FOLLOWING DOCUMENTS
==================================================

# 1. PRODUCT REQUIREMENTS DOCUMENT

File:
`/docs/PRD.md`

Include:
- extension overview
- purpose
- target users
- problems solved
- key workflows
- feature list
- user stories
- permissions justification
- success metrics

==================================================

# 2. CHROME EXTENSION ARCHITECTURE

File:
`/docs/ARCHITECTURE.md`

Include:
- extension architecture
- manifest version
- background/service worker architecture
- popup architecture
- content script architecture
- injected script flow
- browser API usage
- message passing flow
- storage architecture
- external API integrations
- build pipeline

Include Mermaid diagrams.

==================================================

# 3. MANIFEST DOCUMENTATION

File:
`/docs/MANIFEST.md`

Document:
- manifest version
- permissions
- host_permissions
- commands
- action config
- content_scripts
- web_accessible_resources
- CSP configuration
- background/service worker config

Explain why each permission exists.

==================================================

# 4. FEATURE INVENTORY

File:
`/docs/FEATURES.md`

Generate:
- all extension features
- grouped by module
- implementation status:
  - complete
  - partial
  - inferred
  - experimental

==================================================

# 5. UI DOCUMENTATION

File:
`/docs/UI.md`

Include:
- popup pages
- options/settings pages
- onboarding flows
- modals
- injected UI
- routing structure
- component architecture
- state management
- styling system

==================================================

# 6. CONTENT SCRIPT DOCUMENTATION

File:
`/docs/CONTENT_SCRIPTS.md`

Document:
- content scripts
- injected scripts
- DOM manipulation
- mutation observers
- page interaction logic
- iframe handling
- event listeners
- script injection strategy

==================================================

# 7. BACKGROUND SERVICE DOCUMENTATION

File:
`/docs/BACKGROUND.md`

Include:
- background scripts/service workers
- alarms
- listeners
- runtime events
- tabs API usage
- webRequest usage
- lifecycle handling
- notification logic
- job orchestration

==================================================

# 8. STORAGE DOCUMENTATION

File:
`/docs/STORAGE.md`

Include:
- chrome.storage usage
- local/session/sync storage
- IndexedDB usage
- caching
- persistence strategy
- data lifecycle
- storage schema

==================================================

# 9. MESSAGE PASSING DOCUMENTATION

File:
`/docs/MESSAGING.md`

Document:
- runtime messaging
- tab messaging
- communication flows
- background ↔ popup
- popup ↔ content script
- content ↔ injected script
- event contracts

Include diagrams.

==================================================

# 10. SECURITY REVIEW

File:
`/docs/SECURITY.md`

Analyze:
- permission risks
- CSP security
- XSS risks
- injection safety
- token handling
- OAuth flows
- external requests
- storage security
- message validation
- unsafe DOM usage
- sandboxing concerns

Provide recommendations.

==================================================

# 11. API & INTEGRATIONS DOCUMENTATION

File:
`/docs/API.md`

Include:
- external APIs
- authentication methods
- request flows
- rate limiting
- retry logic
- error handling
- webhook/event handling

==================================================

# 12. DEVELOPER SETUP GUIDE

File:
`/docs/ONBOARDING.md`

Include:
- prerequisites
- installation
- extension loading process
- dev mode setup
- build scripts
- local development workflow
- debugging techniques
- hot reload setup

==================================================

# 13. BUILD & RELEASE DOCUMENTATION

File:
`/docs/BUILD_RELEASE.md`

Include:
- build process
- packaging
- Chrome Web Store deployment
- versioning
- CI/CD
- signing/publishing process
- environment separation

==================================================

# 14. TESTING DOCUMENTATION

File:
`/docs/TESTING.md`

Include:
- test frameworks
- unit tests
- integration tests
- E2E tests
- browser testing strategy
- mocked Chrome APIs
- coverage gaps

==================================================

# 15. PROJECT STRUCTURE DOCUMENT

File:
`/docs/PROJECT_STRUCTURE.md`

Generate:
- complete folder explanation
- module boundaries
- important files
- shared utilities
- architectural conventions

==================================================

# 16. TECHNICAL DEBT REPORT

File:
`/docs/TECH_DEBT.md`

Identify:
- duplicated logic
- anti-patterns
- permission overreach
- scalability concerns
- performance bottlenecks
- memory leaks
- dead code
- TODOs
- maintainability issues

==================================================

# 17. PERFORMANCE REVIEW

File:
`/docs/PERFORMANCE.md`

Analyze:
- content script performance
- DOM observation costs
- memory usage
- background worker efficiency
- storage efficiency
- bundle sizes
- lazy loading opportunities

==================================================

# 18. ENVIRONMENT VARIABLES DOCUMENT

File:
`/docs/ENVIRONMENT.md`

Include:
- all environment variables
- purpose
- required/optional
- safe example values

NEVER expose secrets.

==================================================
OUTPUT REQUIREMENTS
==================================================

- Create all documents inside `/docs`
- Use clean Markdown
- Use tables when useful
- Use Mermaid diagrams when useful
- Reference relevant files when helpful
- Keep documentation maintainable and professional

==================================================
IMPORTANT RULES
==================================================

- DO NOT hallucinate features
- DO NOT expose secrets
- DO NOT skip internal scripts
- Infer behavior carefully from code
- Mark assumptions explicitly
- Explain Chrome permissions carefully
- Highlight security risks clearly

==================================================
BONUS DOCUMENTS (OPTIONAL)
==================================================

If enough information exists, also generate:
- `/docs/ROADMAP.md`
- `/docs/SCALABILITY.md`
- `/docs/OBSERVABILITY.md`
- `/docs/CODING_STANDARDS.md`
- `/docs/MULTI_BROWSER_SUPPORT.md`

==================================================
FINAL TASK
==================================================

After generating all documents:
1. Create `/docs/INDEX.md`
2. Link all generated files
3. Add summaries for each document
4. Create a recommended next-steps section

Proceed with full repository analysis and documentation generation.
