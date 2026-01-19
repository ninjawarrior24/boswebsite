# Static site — deploy to GitHub Pages

This repository contains a simple static site (root HTML/CSS/JS). Steps to publish to GitHub Pages:

1. Initialize git and commit your files locally

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
```

2a. Create a new GitHub repository via the website and add it as remote:

```bash
git remote add origin https://github.com/USERNAME/REPO.git
git push -u origin main
```

2b. Or, create and push using the GitHub CLI (`gh`):

```bash
gh repo create USERNAME/REPO --public --source=. --remote=origin --push
```

3. The included GitHub Actions workflow will deploy the repository root to GitHub Pages automatically on push to `main`.

4. After the first successful run, your site will be available at either:

- `https://USERNAME.github.io/REPO/` (for a repo site)

Notes:
- Replace `USERNAME` and `REPO` with your GitHub username and repository name.
- If you prefer a specific branch or a custom domain, adjust settings or add a `CNAME` file.
