# Repository Guidelines

## Project Structure & Module Organization
- Root contains `mint.json` (site config), `README.md`, and content pages (`*.mdx`).
- Sections live in folders such as `api-reference/`, `capabilities/`, `essentials/`, `snippets/`.
- Static assets live in `images/` and `logo/`. Prefer relative paths (e.g., `images/diagram.png`).
- Keep topic-focused pages at the root (e.g., `quickstart.mdx`, `architecture.mdx`). Update navigation in `mint.json` when adding pages.

## Build, Test, and Development Commands
- `npm i -g mintlify` — Install Mintlify CLI (one-time).
- `mintlify dev` — Run local preview server in the repo root.
- `mintlify install` — Reinstall dependencies if the dev server fails to start.
- Deployments are automated via the GitHub App; push to the default branch to publish.

## Coding Style & Naming Conventions
- Filenames: kebab-case with `.mdx` (e.g., `custom-rag-pipeline.mdx`).
- Headings: one H1 per page; start content sections at H2. Use Title Case for titles.
- Indentation: 2 spaces. Wrap lines for readability (~100 chars) where practical.
- Code blocks: fenced with language (e.g., ```ts, ```bash). Prefer runnable snippets.
- Links: relative for internal pages; verify anchors. Images use `![alt](images/...)` with descriptive alt text.

## Testing Guidelines
- Preview locally with `mintlify dev` and click through new/edited pages.
- Validate links, images, and code fences (language, copy-ability). Check browser console for build or MDX errors.
- No unit tests in this repo; treat docs review (content, accessibility, navigation) as the quality gate.

## Commit & Pull Request Guidelines
- Branch names: `docs/<topic>` (e.g., `docs/rag-pipeline-faq`).
- Commit messages: imperative and scoped. Prefer Conventional Commits, e.g., `docs: clarify RAG pipeline inputs`, `fix: broken image path`.
- PRs: include a concise summary, screenshots for visual changes, and links to any related issues. Note nav changes in `mint.json`.

## Security & Configuration Tips
- Do not commit secrets, tokens, or private URLs in examples.
- Sanitize or mock sensitive data in screenshots and code.
- Keep `mint.json` organized; group related pages and ensure new pages are listed.
