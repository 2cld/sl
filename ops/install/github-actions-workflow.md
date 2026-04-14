[edit](https://github.com/2cld/sl/edit/main/ops/install/github-actions-workflow.md)
# GitHub Actions MkDocs Workflow

This document explains the GitHub Actions workflow that builds and deploys the SL documentation site using MkDocs Material theme.

## How It Works

When you push changes to the `main` branch, GitHub Actions automatically:
1. Checks out the repository
2. Installs Python and MkDocs with the Material theme
3. Builds the markdown files into a static HTML site
4. Deploys the built site to the `gh-pages` branch

GitHub Pages then serves the `gh-pages` branch at https://sl.2cld.net.

## Workflow File Explained

The workflow lives at `.github/workflows/mkdocs.yml`.

```yaml
name: Deploy MkDocs to GitHub Pages
```
Display name shown in the GitHub Actions tab.

```yaml
on:
  push:
    branches:
      - main
```
Trigger: runs every time code is pushed to the `main` branch. Pull requests or other branches won't trigger a deploy.

```yaml
permissions:
  contents: write
```
Grants the workflow permission to write to the repository. Required because `mkdocs gh-deploy` pushes the built site to the `gh-pages` branch.

```yaml
jobs:
  deploy:
    runs-on: ubuntu-latest
```
Runs on a fresh Ubuntu virtual machine provided by GitHub (free for public repos).

```yaml
    steps:
      - uses: actions/checkout@v4
```
Checks out your repository code so the workflow can access the markdown files and mkdocs config.

```yaml
      - uses: actions/setup-python@v5
        with:
          python-version: '3.x'
```
Installs the latest Python 3.x on the runner. MkDocs requires Python.

```yaml
      - run: pip install mkdocs-material
```
Installs MkDocs and the Material theme. The `mkdocs-material` package includes `mkdocs` as a dependency.

```yaml
      - run: mkdocs gh-deploy --force --config-file .mkdocs/mkdocs.yml
```
Builds the site and pushes it to the `gh-pages` branch.
- `--force` overwrites the gh-pages branch completely each time
- `--config-file .mkdocs/mkdocs.yml` points to our config (which is in a subfolder because mkdocs requires docs_dir to be a child of the config location)

## MkDocs Configuration

The config lives at `.mkdocs/mkdocs.yml` and controls:
- `docs_dir: ..` - tells mkdocs to look for markdown files in the repo root
- `site_dir: ../site` - where the built HTML goes (locally)
- `nav:` - defines the sidebar navigation structure
- `theme:` - Material theme with dark mode and search

## GitHub Pages Settings

After the first workflow run, configure GitHub Pages:
1. Go to repo Settings > Pages
2. Set Source to **Deploy from a branch**
3. Set Branch to **gh-pages** / **(root)**
4. Save

The CNAME file is automatically copied to the gh-pages branch by mkdocs.

## How to Revert to Plain GitHub Pages

If you want to go back to GitHub serving raw markdown (no MkDocs):

### Step 1: Change GitHub Pages source branch
1. Go to repo **Settings** > **Pages**
2. Change Branch from `gh-pages` to `main`
3. Set folder to `/ (root)`
4. Click **Save**

### Step 2: Disable the workflow
Either delete `.github/workflows/mkdocs.yml` or disable it:
1. Go to repo **Actions** tab
2. Click on "Deploy MkDocs to GitHub Pages" workflow
3. Click the `...` menu > **Disable workflow**

### Step 3: (Optional) Delete the gh-pages branch
```bash
git push origin --delete gh-pages
```

After these steps, GitHub Pages will serve your raw markdown files directly from the main branch, just like before.

## Local Preview

To preview the site locally before pushing:
```bash
pip install mkdocs-material
python -m mkdocs serve -f .mkdocs/mkdocs.yml
```
Then open http://127.0.0.1:8000 in your browser.
