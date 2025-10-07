
# Project Management System

A lightweight, React-based Project Management System built with Create React App. This repository contains a client-side single-page application (SPA) that provides project, task, activity feed, file management, and reporting views for team collaboration and project tracking.

## Key Features

- User authentication (login/register) - UI scaffolding in `src/components/Login.js` and `src/components/Register.js`.
- Project list and detail pages (`Projects.js`, `ProjectProgressPage.js`).
- Task management with comments (`Tasks.js`, `TaskComments.js`).
- Activity feed and notifications (`ActivityFeed.js`, `Notifications.js`).
- Gantt chart view for scheduling (`GanttChartPage.js`).
- File management and downloads (pages in `src/pages/FileManagement.js`).
- Risk & issue reporting (`src/pages/RiskAndIssueManagement.js`).

## Tech Stack

- React (Create React App)
- JavaScript (ES6+)
- CSS modules / plain CSS (styles under `src/`)
- No backend in this repository — intended as a frontend client to be connected to an API

## Project structure

Top-level files and key folders:

- `public/` — static assets and `index.html`.
- `src/` — React source files, components, pages, and CSS.
	- `src/components/` — reusable components (Dashboard, Tasks, Projects, Login, Register, etc.).
	- `src/pages/` — full-page views (FileManagement, RiskAndIssueManagement).
	- `src/assets/` — images and static assets.

Example important files:

- `src/index.js` — app entry point.
- `src/App.js` — app shell and routing.
- `src/components/Dashboard.js` — main dashboard view.

## Getting started (development)

Prerequisites:

- Node.js (LTS recommended) and npm installed on your machine.

Install dependencies:

```powershell
cd "d:\New folder\Project Management System"
npm install
```

Start the development server:

```powershell
npm start
```

Open http://localhost:3000 in your browser. The app will hot-reload on file changes.

## Build for production

To create an optimized production build:

```powershell
npm run build
```

This generates a `build/` folder suitable for deployment to a static host or to be served by a backend.

## Testing

This project includes the default Create React App test setup. To run tests:

```powershell
npm test
```

## Development notes & integration points

- This repository currently contains the frontend only. To use this app in a real environment you will need to connect it to a backend API for authentication, projects, tasks, files, and notifications.
- Recommended backend endpoints:
	- POST /auth/login
	- POST /auth/register
	- GET /projects
	- GET /projects/:id
	- GET /projects/:id/tasks
	- POST /tasks/:id/comments
	- GET /activity
- Add an HTTP client (axios or fetch wrappers) and environment configuration for API base URL in `src/`.

## Styling and assets

- Styles are located alongside components as CSS files (`*.css`).
- Replace placeholder images in `src/assets/` and `public/` as needed.

## Contributing

Contributions are welcome. Suggested workflow:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/your-feature`.
3. Make changes, add tests where applicable.
4. Open a pull request with a clear description of changes.

Before opening a PR, ensure the app builds and tests pass.

## License

Include your project license here (e.g., MIT). If you want, I can add a sample `LICENSE` file.

## Contact / Support

If you need help integrating a backend, adding authentication, or preparing this app for production, tell me what you want and I can implement or scaffold it.

---

Last updated: 2025-10-07
