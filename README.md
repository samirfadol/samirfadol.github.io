# Samir A. Fadol — Academic Website

Personal academic website built with [Hugo](https://gohugo.io/) and deployed to GitHub Pages.

**Live site (after deployment):** https://samirfadol.github.io/

## Local preview

```bash
hugo server -D
```

Then open http://localhost:1313/

## Build

```bash
hugo --gc --minify
```

Output goes to `public/`.

## Updating content

See [UPDATING.md](UPDATING.md) for plain-language instructions on editing papers, bio, CV, and other content directly on GitHub.

## Repository setup (first-time deployment)

1. Create a GitHub repository named `samirfadol.github.io` under the `samirfadol` account.
2. Push this code to the `main` branch.
3. In GitHub repo Settings → Pages, set Source to **GitHub Actions**.
4. The site will build and deploy automatically on every push to `main`.
