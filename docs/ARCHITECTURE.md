# Feego — Initial Architecture

## Design Goal

Feego is planned as a modular personal assistant. The first implementation should remain small and local-first, with clear boundaries between the agent core, storage, interfaces, and external services.

## High-Level Components

```text
                 Mobile / Desktop UI
                         |
Chrome Extension --- Agent Interface
                         |
                    Agent Core
                   /     |     \
              Tasks  Reminders  Knowledge
                   \     |     /
                    Local Storage
                      SQLite
                         |
                 Integration Layer
                  /            \
              Email API      SMS API
```

This is a conceptual direction, not an implemented system diagram.

## Proposed Responsibilities

### Agent Core

- Coordinate user requests and application services.
- Validate inputs and apply user-defined rules.
- Keep business logic independent from the user interface.

### Task and Reminder Services

- Create, update, complete, and remove tasks.
- Schedule reminders and track their delivery state.
- Avoid duplicate reminder delivery where practical.

### Personal Knowledge

- Start with user-managed notes and structured preferences.
- Keep data inspectable and editable.
- Consider semantic or AI-assisted retrieval only after the basic system is reliable.

### Storage

- Use SQLite for the initial local implementation.
- Keep database access behind a small persistence layer.
- Plan explicit backup and restore behavior.

### Integration Layer

- Isolate email and SMS providers behind replaceable adapters.
- Store credentials in environment variables or a secure platform store.
- Make external actions visible and configurable.

### User Interfaces

- Flutter is the current direction for mobile and desktop UI.
- A Chrome extension will provide browser integration.
- Interfaces should communicate with the agent through a documented API or local service boundary.

## Initial Technology Direction

- Python: agent core and backend
- SQLite: local persistence
- Flutter: mobile and desktop UI
- Chrome Extensions: browser integration
- Email/SMS APIs: outbound notifications

These are initial choices and may change as implementation requirements become clearer.

## Security and Privacy Principles

- Never commit secrets or real user data.
- Request permission before sending messages or performing consequential external actions.
- Prefer local storage for personal information when practical.
- Document what data leaves the device when external integrations are enabled.
