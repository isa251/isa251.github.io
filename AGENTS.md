# Repository Guidelines

## Project Structure & Module Organization
This is a single-file static site. The core UI, styles, and behavior live in `index.html`. GitHub Pages deployment is configured in `.github/workflows/static.yml`. If you add assets (images, videos), keep them in a top-level folder like `assets/` and use relative paths from `index.html`.

## Build, Test, and Development Commands
There is no build step. For a local preview, serve the repo with a simple static server:
```sh
python3 -m http.server 8000
```
Then open `http://localhost:8000` in a browser. You can also open `index.html` directly, but a server is closer to GitHub Pages behavior.

## Coding Style & Naming Conventions
Keep indentation at 2 spaces, matching `index.html`. Use descriptive, lowercase CSS class names (e.g., `.bookRig`, `.spreadWrap`) and prefer CSS variables under `:root` for theme values. In JavaScript, keep constants in `SCREAMING_SNAKE_CASE` (e.g., `PAGES`, `ORDER`) and functions in `camelCase`. Content strings can be bilingual; keep line breaks intentional since they are rendered into HTML.

## Testing Guidelines
No automated tests are configured. Validate changes manually:
- Open the page on desktop and mobile widths (<= 760px) to verify layout and page-flip behavior.
- Confirm external embeds (e.g., YouTube if used) load correctly.

## Commit & Pull Request Guidelines
Existing commits use short, descriptive messages, often in Japanese (e.g., `更新`). Follow that style: concise, imperative, and focused on the change. For pull requests, include a brief summary and screenshots or screen recordings for visual/UI updates. Link related issues when available.

## Deployment
Pushes to `main` trigger GitHub Pages via `.github/workflows/static.yml`. Ensure the page renders correctly before merging.
