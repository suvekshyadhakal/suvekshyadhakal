# Publish Suvekshya’s GitHub profile README

## What this package contains

- `README.md`: recruiter-friendly GitHub profile with accurate project metrics, tech stack and leadership.
- `assets/hero.svg`: animated custom header (no external image hosting or JavaScript).
- `assets/pipeline.svg`: animated “ingest → denoise → model → validate → explain” diagram.
- `.github/workflows/snake.yml`: daily contribution-snake image generator for light/dark mode.

## One-time setup

1. Sign in to GitHub as **suvekshyadhakal**.
2. Create a **public** repository named **`suvekshyadhakal`** (exactly your username). GitHub recognizes `username/username` as your profile README repository.
3. Add *all* files and folders from this package to the repo. Keep `README.md` at the root, and preserve `.github/workflows/snake.yml`.
   - Easy path: create repo **without initializing** a README, clone it, copy these files, then `git add . && git commit -m "Build animated AI profile" && git push -u origin main`.
   - Alternatively, use the GitHub web interface to upload the README and the two SVGs, and separately create the workflow file at `.github/workflows/snake.yml`.
4. Go to **Settings → Actions → General → Workflow permissions** and ensure GitHub Actions has **Read and write permissions** if your account/org settings require that. This lets the workflow publish generated assets to its `output` branch.
5. In **Actions → Animate contribution graph**, choose **Run workflow**. Wait for the workflow to succeed. It should create the `output` branch with `github-snake.svg` and `github-snake-dark.svg`.
6. Edit `README.md`: remove the HTML comment wrapper around the final `07 / GITHUB ACTIVITY` section (remove the lines starting `<!-- CONTRIBUTION SNAKE...` and ending `-->`). Commit this update.
7. Visit **https://github.com/suvekshyadhakal** and inspect both light and dark modes.

## Content accuracy / limits

This README uses the currently supplied resume and directly provided claims. There are **no invented GitHub projects, repository URLs, deployment claims, or employment claims**. Model metrics come from the resume and should be updated if you rerun evaluation or identify leakage/data split issues.

The connector returned username `suvekshyadhakal` but **no GitHub App installations or accessible repositories**, and `suvekshyadhakal/suvekshyadhakal` was not found. For that reason the package was prepared locally; it was *not* published to GitHub in the creation session. If you want the assistant to edit it in future, connect the GitHub app to the profile repository with repo read/write permissions.

## Customization tips

- When you publish a project repo, add **real** GitHub links to its card in `README.md`.
- Add a LinkedIn badge only after replacing it with your verified personal URL.
- Avoid posting your phone number publicly; this package intentionally includes email contact only.
- GitHub renders repo SVGs as images; animation support can vary by platform and reduced-motion settings.
- The README is intentionally not dependent on GitHub stats widgets that may be unavailable/rate-limited or show misleading new-account metrics.
