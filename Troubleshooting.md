# Troubleshooting

## Build error: "Expected '>', got 'className'"
Cause: JSX inside a .ts file.
Fix: rename the file to .tsx (example: registry.ts → registry.tsx).

## Module not found "@/src/..."
Cause: Your alias "@/..." already points to /src.
Fix: Use "@/lib/..." instead of "@/src/lib/...".

## Control Center 404
Cause: Missing route file.
Fix: create:
- app/admin/core/page.tsx

## Installs not showing
Cause: Installs are per workspaceId in localStorage.
Fix:
- ensure workspaceId matches the one used during install
- refresh the page

