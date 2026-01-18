# Architecture (Phase 1)

## Core Concepts

### Core
Core is the runtime layer. It should remain stable.
Core responsibilities:
- App registry contract (type definitions + app entries)
- Install store (localStorage in Phase 1)
- Workspace app manager UI (install/enable/disable)
- Workspace runner/gate route (loads app component)

### Modules / Apps
Modules (apps) are optional features added to core by registering in the App Registry.

Each app defines:
- id, name, icon, description
- required tier (Phase 1 metadata only)
- routes (links)
- component entry (React component rendered by runner)

### Widgets
Widgets are embeddable UI blocks that can appear inside dashboards.
Phase 1: only a concept and optional placeholder toggles.
Phase 2+: modules register widgets; core renders them in “placements”.

## Phase 1 Data Flow

1) Core reads the registry to show the list of available apps.
2) User installs an app into a workspace → install store writes to localStorage.
3) User opens /apps/[appId] → runner checks install store:
   - not installed → show install prompt
   - disabled → show disabled state
   - active → render app component

## Current Storage Strategy (Phase 1)
- localStorage
- scoped by workspaceId
- zero backend dependency

