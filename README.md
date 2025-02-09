# AI Agents Landing Page

This project is a futuristic, interactive landing page for AI Agents, built with React, Tailwind CSS, Framer Motion, and Three.js.

## Table of Contents

- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running Locally](#running-locally)
- [Dependencies](#dependencies)
- [Deployment (Netlify)](#deployment-netlify)
  - [Build Command](#build-command)
  - [Publish Directory](#publish-directory)
- [Troubleshooting](#troubleshooting)

## Project Structure

```
ai-agents-landing-page/
├── public/
│   └── vite.svg
├── src/
│   ├── components/
│   │   ├── AgentCard.jsx
│   │   ├── AgentsShowcase.jsx
│   │   ├── AnimatedGradient.jsx
│   │   ├── Features.jsx
│   │   ├── Footer.jsx
│   │   ├── Hero.jsx
│   │   ├── Modal.jsx
│   │   └── NeonGrid.jsx
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── index.html
├── package.json
├── postcss.config.cjs
├── tailwind.config.cjs
└── vite.config.js (if applicable, created by Vite)
```

## Getting Started

### Prerequisites

-   Node.js (LTS version recommended)
-   npm (comes with Node.js)

### Installation

1.  Clone the repository (not applicable in WebContainers):
    ```bash
    # This step is not applicable in the WebContainer environment.
    # git clone <repository-url>
    # cd ai-agents-landing-page
    ```

2.  Install dependencies:
    ```bash
    npm install
    ```

### Running Locally

To start the development server:

```bash
npm run dev
```

This will start the Vite development server, and you can view the landing page in your browser (usually at `http://localhost:5173` or similar).  The page will automatically reload when you make changes to the source code.

## Dependencies

The project uses the following key dependencies:

-   **`@react-three/drei`:**  Helper components and utilities for React Three Fiber.
-   **`@react-three/fiber`:**  React renderer for Three.js.
-   **`framer-motion`:**  Animation library for React.
-   **`leva`:**  GUI controls library (optional, can be removed if not used).
-   **`react`:**  JavaScript library for building user interfaces.
-   **`react-dom`:**  Provides DOM-specific methods for React.
-   **`react-icons`:**  Popular icon library for React.
-   **`react-intersection-observer`:**  React implementation of the Intersection Observer API.
-   **`three`:**  3D graphics library.
-   **`autoprefixer`:**  PostCSS plugin to parse CSS and add vendor prefixes.
-   **`postcss`:**  Tool for transforming CSS with JavaScript.
-   **`tailwindcss`:**  Utility-first CSS framework.
-   **`vite`:**  Fast build tool and development server.

These dependencies are listed in the `package.json` file and will be installed when you run `npm install`.

## Deployment (Netlify)

To deploy this project to Netlify, follow these steps:

1.  **Push your code to a Git repository** (e.g., GitHub, GitLab, Bitbucket).  (Again, not directly applicable in the WebContainer, but important for real-world deployment.)
2.  **Create a new site on Netlify:**
    -   Log in to your Netlify account.
    -   Click "New site from Git".
    -   Choose your Git provider and select the repository.
3.  **Configure Netlify settings:**
    -   **Branch to deploy:**  `main` (or your primary branch)
    -   **Build command:** `npm run build`
    -   **Publish directory:** `dist`

### Build Command

The build command tells Netlify how to build your project.  `npm run build` uses Vite to create an optimized production build of your application in the `dist` directory.

### Publish Directory

The publish directory is the folder that contains the built files that Netlify should serve.  Vite, by default, outputs the production build to the `dist` folder.

4.  **Deploy Site:** Click the "Deploy site" button. Netlify will build and deploy your site. You'll get a unique URL where your landing page is live.

## Troubleshooting
- **Dependency Conflicts:** If you encounter dependency conflicts during installation, you might need to adjust the versions of the packages in `package.json` to ensure compatibility.  You can also try using the `--force` or `--legacy-peer-deps` flags with `npm install`, but this is generally not recommended unless you understand the potential consequences.
- **Three.js Errors:** If you see errors related to Three.js or `@react-three/fiber`, double-check that you're using compatible versions of these libraries and that you're using hooks correctly (inside the `<Canvas>` component).
- **Netlify Build Failures:** If your Netlify build fails, check the deploy logs for error messages. Common issues include incorrect build commands, missing dependencies, or problems with your code.
- **CSS Issues:** Ensure that your Tailwind CSS classes are being correctly applied. If you're using custom CSS, make sure it's being imported correctly.
- **Modal Not Showing:** If the modal is not appearing, double-check the `isOpen` state and the `onClick` handlers of the buttons that should trigger the modal.
