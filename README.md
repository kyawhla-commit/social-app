# Social App

A React frontend for the Social API - a social media platform with posts, comments, and likes.

## Features

- User authentication (login/register)
- View and create posts
- Comment on posts
- Like/unlike posts
- Dark/light theme toggle
- Responsive Material UI design

## Tech Stack

- **Framework:** React 18
- **Build Tool:** Vite
- **UI Library:** Material UI (MUI) 7
- **Routing:** React Router 7
- **State Management:** TanStack React Query
- **Forms:** React Hook Form

## Getting Started

### Prerequisites

- Node.js 18+
- npm
- Social API running on `http://localhost:8800`

### Installation

```bash
# Install dependencies
npm install
```

### Running the App

```bash
# Development server
npm run dev
```

The app runs on `http://localhost:5173`

### Build for Production

```bash
npm run build
npm run preview
```

## Project Structure

```
src/
├── components/       # Reusable UI components
│   ├── AppDrawer.jsx
│   ├── Comment.jsx
│   ├── Form.jsx
│   ├── Header.jsx
│   └── Post.jsx
├── pages/            # Route pages
│   ├── Login.jsx
│   ├── Posts.jsx
│   ├── Profile.jsx
│   ├── Register.jsx
│   └── View.jsx
├── App.jsx           # Main app layout
├── AppProvider.jsx   # Context providers (theme, auth, query)
└── main.jsx          # Entry point with routing
```

## Routes

| Path | Description |
|------|-------------|
| `/` | Home - Posts feed |
| `/view/:id` | Single post view with comments |
| `/login` | User login |
| `/register` | User registration |

## Configuration

The API endpoint is configured in `src/AppProvider.jsx`:

```javascript
const api = "http://localhost:8800";
```

Update this if your API runs on a different host/port.
