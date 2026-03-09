# Modern Login Page

A clean, modern login page built with HTML, CSS, and vanilla JavaScript featuring a **glassmorphism** design and animated background.

## Preview

![Login Page Preview](bg.jpg)

## Features

- **Glassmorphism UI** — frosted glass card with backdrop blur and semi-transparent border
- **Animated background** — continuous hue-rotation animation on the background image
- **Floating labels** — input labels smoothly animate upward on focus/input
- **Ionicons** — mail and lock icons inside the input fields
- **Form validation** — client-side checks for empty fields; password enforces 8–16 character length
- **Remember Me** — checkbox to persist session preference
- **Responsive design** — adapts to mobile screens (≤ 480px), expanding to full viewport
- **GitHub Pages deployment** — automated CI/CD via GitHub Actions on every push to `main`

## Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and form markup |
| CSS3 | Glassmorphism styling, animations, responsive layout |
| JavaScript (ES6) | Form validation and submission handling |
| [Poppins](https://fonts.google.com/specimen/Poppins) | Google Font used throughout |
| [Ionicons v7](https://ionic.io/ionicons) | Mail and lock icons |
| GitHub Actions | Automated deployment to GitHub Pages |

## File Structure

```
ModerLogInPage/
├── index.html          # Main HTML file with form and inline JS
├── style.css           # All styles including animations and responsive rules
├── bg.jpg              # Background image (hue-rotated via CSS animation)
├── login.png           # Favicon
└── .github/
    └── workflows/
        └── deploy.yml  # GitHub Actions workflow for GitHub Pages deployment
```

## Getting Started

### Run Locally

No build tools required. Simply open the file in a browser:

```bash
# Clone the repository
git clone https://github.com/<your-username>/<repo-name>.git

# Open in browser
start index.html        # Windows
open index.html         # macOS
xdg-open index.html     # Linux
```

Or use the **Live Server** extension in VS Code for hot-reload during development.

### Deploy to GitHub Pages

Deployment is fully automated. Every push to the `main` branch triggers the [deploy.yml](.github/workflows/deploy.yml) workflow which:

1. Checks out the repository
2. Configures GitHub Pages
3. Uploads all files as a deployment artifact
4. Publishes to your GitHub Pages URL

Manually trigger a deployment from the **Actions** tab using the `workflow_dispatch` event.

## Form Behaviour

- Both **Email** and **Password** fields are required
- Password must be **8–16 characters** long (enforced via HTML `minlength`/`maxlength` and JS trim validation)
- On successful submission an `alert("Login Successful!")` is shown (replace with a real backend call in production)
- A commented-out `fetch` snippet is included as a starting point for API integration

## Customisation

| What to change | Where |
|---|---|
| Background image | Replace `bg.jpg` |
| Animation speed | `animation: animateBg 5s` in `style.css` |
| Card dimensions | `.login-box` width/height in `style.css` |
| Colour scheme | Update `rgba`/`#fff` values in `style.css` |
| Backend endpoint | Uncomment and update the `fetch` call in `index.html` |

## License

This project is open source and available under the [MIT License](LICENSE).
