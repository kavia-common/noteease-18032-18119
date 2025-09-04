# NoteEase — Svelte Frontend

Minimalistic, light-themed note taking UI with:
- Create notes
- Edit notes
- Delete notes
- List all notes
- Search notes

Layout:
- Sidebar (search, create, list)
- Main area (editor)

Colors:
- Primary: #1976d2
- Secondary: #424242
- Accent: #ff4081

## Development

Install dependencies and run:

```bash
npm install
npm run dev
```

Open the app at http://localhost:3000.

## Backend Integration

This app is intended to connect to a notes database backend (dependency: notes_database).

- Set the API base URL in your environment:
  - Vite uses `VITE_*` envs.
  - Create a `.env` file at the project root with:

```
VITE_NOTES_API_URL=https://your-notes-backend.example.com
```

Endpoints expected by the API client (can be adapted):
- GET    /notes           -> Note[]
- POST   /notes           -> Note
- PUT    /notes/:id       -> Note
- DELETE /notes/:id       -> 204

If `VITE_NOTES_API_URL` is not set, the app runs in demo mode:
- Data is stored in localStorage.
- API calls are simulated.

## Project structure

- src/lib/components
  - Sidebar.svelte
  - Editor.svelte
- src/lib/stores
  - notes.ts
- src/lib/services
  - api.ts
- src/lib/styles
  - theme.css
- src/routes
  - +layout.svelte
  - +page.svelte

## Accessibility and UX

- Keyboard focus and Enter key support on list items.
- Autosave on blur and explicit Save button.
- Minimal color accents and clear visual hierarchy.

