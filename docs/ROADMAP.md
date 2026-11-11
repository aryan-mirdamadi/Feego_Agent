# Feego Development Roadmap

This roadmap describes the intended development sequence. Items are plans, not claims of completed functionality.

## Phase 0 — Project Foundation

- [x] Create the public repository
- [x] Establish project overview and development principles
- [x] Document the initial architecture direction
- [x] Define the first development milestones

## Phase 1 — Minimal Agent Core

- [ ] Set up the Python project and development environment
- [ ] Define task and reminder data models
- [ ] Add local SQLite persistence
- [ ] Implement task creation, listing, completion, and deletion
- [ ] Add a reliable reminder scheduler
- [ ] Write basic automated tests

## Phase 2 — Notifications

- [ ] Add configurable email notifications
- [ ] Design an SMS provider interface
- [ ] Add notification preferences and delivery status
- [ ] Keep credentials outside source control

## Phase 3 — Personal Memory and Manual Knowledge

- [ ] Define a simple local knowledge format
- [ ] Allow users to add, edit, and remove knowledge manually
- [ ] Add searchable personal notes and preferences
- [ ] Document backup and restore behavior

## Phase 4 — User Interfaces

- [ ] Build the first mobile interface
- [ ] Add task and reminder views
- [ ] Add customizable wallpapers, images, and clock settings
- [ ] Evaluate desktop support

## Phase 5 — Browser Integration

- [ ] Build a minimal Chrome extension
- [ ] Connect the extension to the local or remote agent interface
- [ ] Add user-controlled browser actions

## Phase 6 — Optional Advanced Intelligence

- [ ] Define a provider-independent AI integration layer
- [ ] Add optional language-model capabilities
- [ ] Make permissions and user confirmation explicit for consequential actions

## Guiding Rule

Prioritize a dependable, understandable task-and-reminder assistant before adding complex autonomous behavior.
