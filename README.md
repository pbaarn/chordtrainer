# Cadence - Premium Piano Chord Recall Trainer

A professional, interactive web application to practice piano chord recall, intervals, extended harmonies, and ear training.

Hosted on GitHub Pages at: [https://pbaarn.github.io/chordtrainer/](https://pbaarn.github.io/chordtrainer/)

---

## 🚀 GitHub Pages Deployment Guide

If you want to host a single-file HTML web application (like this one) on GitHub Pages in the future, follow these instructions.

### Why did the initial build fail?
GitHub Pages defaults to building sites using **Jekyll** (a static site generator). Jekyll failed to build the repository for two reasons:
1. **No Entrypoint:** It looks for an `index.html` file at the root of the repository to serve as the homepage. Your main file was named `piano_chord_recall_trainer.html`.
2. **Liquid Parsing Error:** The HTML file uses React. React JSX uses double curly braces (`{{` and `}}`) for inline styling and evaluation (e.g., `style={{ height: ... }}`). Jekyll interprets these double curly braces as Liquid template tags and fails to compile the site when it finds invalid Liquid syntax.

---

### How to set up a static HTML site on GitHub Pages next time:

#### Step 1: Prepare Your Files
1. **Name your entrypoint `index.html`**:
   Rename your main HTML file to `index.html` so GitHub Pages knows what page to display when someone visits `https://<username>.github.io/<repository-name>/`.
2. **Add a `.nojekyll` file**:
   Create an empty file named `.nojekyll` at the root of your repository. 
   * *What it does:* This tells GitHub Pages to bypass Jekyll entirely and serve your files statically as-is. This fixes any build errors caused by JSX or template syntax (such as React `style={{...}}`).

#### Step 2: Push to GitHub
Stage, commit, and push your changes to your remote repository:
```bash
git add index.html .nojekyll
git commit -m "Configure for GitHub Pages hosting"
git push origin main
```

#### Step 3: Enable GitHub Pages in GitHub Settings
1. Go to your repository page on GitHub (e.g., `https://github.com/pbaarn/chordtrainer`).
2. Click on the **Settings** tab (gear icon at the top right).
3. In the left sidebar under the "Code and automation" section, click on **Pages**.
4. Under **Build and deployment**:
   * **Source**: Select **Deploy from a branch**.
   * **Branch**: Select `main` (or whichever branch you want to host) and select `/ (root)` as the folder.
5. Click **Save**.
6. Wait 1–2 minutes. GitHub will display a banner at the top of the Pages settings page showing your live URL (e.g., `https://pbaarn.github.io/chordtrainer/`).
