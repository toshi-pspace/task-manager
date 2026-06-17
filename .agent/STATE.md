# State — Task Manager
Updated: 2026-06-17 by claude

## Now
Working version built and restyled. The app is a SINGLE self-contained file:
src/index.html (CSS + JS inline). This fixed an earlier bug where separate
style.css/app.js didn't load in the preview (black-on-black, Add button dead).
Add tasks, check off, delete, clear completed. Persists via localStorage.
Forces light color-scheme so it can't render dark-on-dark.

## Next
- [ ] Try it: open src/index.html in a browser
- [ ] (optional) Add task editing (click text to rename)
- [ ] (optional) Add filters: All / Active / Done
- [ ] (optional) Connect to GitHub + Replit using docs/guides/replit-sync.md

## Open questions
- Keep it local-only (localStorage), or eventually add a backend to sync across devices?

## Don't forget
- This is the user's first Claude Code project — keep things simple and explained.
- No frameworks yet; deliberately plain so it runs by just opening the file.
