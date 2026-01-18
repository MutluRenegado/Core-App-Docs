# Getting Started (Phase 1)

## Requirements
- Node.js (LTS recommended)
- npm

## Install & Run
1. Install dependencies:
   npm install

2. Start dev server:
   npm run dev

## Key URLs
- Control Center:
  /admin/core

- Workspace App Manager:
  /admin/workspace/[workspaceId]/apps

- Workspace App Runner (Gate):
  /admin/workspace/[workspaceId]/apps/[appId]

## Workspace ID
Phase 1 uses a string `workspaceId` from the URL.
Installs are stored per workspace in localStorage with keys like:
- installedApps:<workspaceId>

Example workspace IDs you can use:
- test
- demo
- w1

