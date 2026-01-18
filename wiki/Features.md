# Features (Phase 1)

## Core Runtime
- Central **App Registry** defines apps, metadata, routes, and the component entry point.
- **Install Store (localStorage)** tracks installed apps per workspace.
- **Enable/Disable** per app per workspace.
- **Workspace App Runner / Gate** ensures:
  - if app is not installed → show install UI
  - if installed but disabled → show disabled state
  - if active → render app component

## Admin: Control Center
- A single admin page for managing apps by workspace:
  - list apps from registry
  - install
  - enable/disable
  - open app pages

## Navigation Helpers
- Optional route bridge / generated route listing (dev navigation helper).

## What Phase 1 Does Not Include
- Stripe billing enforcement
- Team roles/permissions enforcement
- Firestore persistence
- Production-grade module discovery

