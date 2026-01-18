# Widgets (Phase 1)

## Definition
A widget is a small embeddable UI block (card, list, stats tile).
Widgets are intended to be provided by modules and rendered by core in predefined placements.

## Phase 1 Status
- Widgets are not required to run the core runtime.
- Phase 1 may include placeholder widget toggles, but widgets are not integrated into core pages by default.

## Phase 2 Direction
- Create a Widget Registry similar to the App Registry
- Modules register widgets
- Core renders them by placement, filtered by:
  - workspace install status
  - enabled widgets list
  - tier/permissions (later)

## Suggested Placements
- workspace.home.top
- workspace.home.grid
- platform.dashboard
- admin.overview

