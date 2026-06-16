# FlowBoard

A modern Kanban-style project management platform built with React, TypeScript, Redux Toolkit, and DnD Kit.

FlowBoard helps individuals and teams organize work, track progress, and collaborate efficiently through boards, lists, and cards. The project is being built as a production-grade frontend application with a focus on scalable architecture, performance, accessibility, and real-time collaboration.

## Goals

This project is designed to explore and implement frontend engineering concepts, including:

- Feature-driven architecture
- Scalable state management
- Drag-and-drop interactions
- Optimistic UI updates
- Real-time collaboration
- Offline-first capabilities
- Frontend performance optimization
- System design patterns used in large-scale React applications

## Features

### Board Management

- Create boards
- Rename boards
- Delete boards

### List Management

- Create lists
- Rename lists
- Delete lists
- Reorder lists

### Card Management

- Create cards
- Edit cards
- Delete cards
- Move cards across lists
- Reorder cards within lists

### Drag and Drop

- Card reordering
- Card movement between lists
- List reordering

### Planned Features

- Card details modal
- Labels and tags
- Due dates
- Checklists
- Search and filtering
- User authentication
- Real-time collaboration
- Offline support
- Activity history
- AI-powered task breakdown and planning

## Tech Stack

### Frontend

- React
- TypeScript
- Vite

### State Management

- Redux Toolkit
- Redux DevTools

### Routing

- React Router

### Drag and Drop

- DnD Kit

### Backend (Planned)

- Node.js
- Express
- PostgreSQL
- Prisma

### Realtime (Planned)

- WebSockets
- Socket.io

## Architecture

FlowBoard follows a feature-first architecture.

src/
├── app/
├── features/
│ ├── boards/
│ ├── lists/
│ └── cards/
├── shared/
└── pages/

The application uses normalized state management to ensure efficient updates and predictable rendering behavior.

Example:

boards
lists
cards

instead of deeply nested structures.

## Project Roadmap

### v1

- Board UI
- List UI
- Card UI

### v2

- Card Drag & Drop

### v3

- List Drag & Drop

### v4

- Card Details

### v5

- Search & Filters

### v6

- Backend Integration

### v7

- Authentication

### v8

- Real-time Collaboration

### v9

- Offline Support

### v10

- AI Productivity Features

## Performance Objectives

The project is intentionally designed to handle:

- Large boards
- Hundreds of cards
- Frequent drag-and-drop operations
- Real-time updates from multiple users

Performance optimizations will include:

- Memoization strategies
- Normalized state
- Virtualized rendering
- Selector optimization
- Render profiling

## Getting Started

Install dependencies:

npm install

Start development server:

npm run dev

Build production bundle:

npm run build

Run linting:

npm run lint

# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
    globalIgnores(['dist']),
    {
        files: ['**/*.{ts,tsx}'],
        extends: [
            // Other configs...

            // Remove tseslint.configs.recommended and replace with this
            tseslint.configs.recommendedTypeChecked,
            // Alternatively, use this for stricter rules
            tseslint.configs.strictTypeChecked,
            // Optionally, add this for stylistic rules
            tseslint.configs.stylisticTypeChecked,

            // Other configs...
        ],
        languageOptions: {
            parserOptions: {
                project: ['./tsconfig.node.json', './tsconfig.app.json'],
                tsconfigRootDir: import.meta.dirname,
            },
            // other options...
        },
    },
]);
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x';
import reactDom from 'eslint-plugin-react-dom';

export default defineConfig([
    globalIgnores(['dist']),
    {
        files: ['**/*.{ts,tsx}'],
        extends: [
            // Other configs...
            // Enable lint rules for React
            reactX.configs['recommended-typescript'],
            // Enable lint rules for React DOM
            reactDom.configs.recommended,
        ],
        languageOptions: {
            parserOptions: {
                project: ['./tsconfig.node.json', './tsconfig.app.json'],
                tsconfigRootDir: import.meta.dirname,
            },
            // other options...
        },
    },
]);
```

