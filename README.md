# Aashima Khanna — Portfolio Website

A personal portfolio built with **Quarto + R**, designed to be edited in **VS Code** and hosted on **GitHub Pages**.

## 1. Install software

- [VS Code](https://code.visualstudio.com/)
- [R](https://cran.r-project.org/)
- [Quarto CLI](https://quarto.org/docs/get-started/)
- VS Code extensions: **Quarto** and **R** (search in Extensions)
- Git (if not already installed)

Check your installation in the VS Code terminal:

```bash
R --version
quarto --version
git --version
```

## 2. Open and preview

Open this folder in VS Code (**File → Open Folder**). In the integrated terminal:

```bash
quarto preview
```

Quarto opens a local preview and updates it as you edit `.qmd` or CSS files. To generate the production files locally:

```bash
quarto render
```

The built site is saved to `_site/`. No RStudio is required. R is used by the executable chart on the Projects page.

## 3. Create GitHub repository and push

Create a new **empty** GitHub repository (for example `portfolio`), without initializing a README. Then run from this folder:

```bash
git init
git add .
git commit -m "Create Quarto portfolio website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

Replace `YOUR_USERNAME` and `YOUR_REPO` with your actual GitHub account and repository names. Authenticate using your normal GitHub sign-in or credential manager.

## 4. Deploy with GitHub Pages

1. In the GitHub repo, open **Settings → Pages**.
2. Under **Build and deployment → Source**, select **GitHub Actions**.
3. Push to `main` or manually run **Actions → Publish Quarto site → Run workflow**.
4. After deployment, visit `https://YOUR_USERNAME.github.io/YOUR_REPO/`.
5. Update `website.site-url` in `_quarto.yml` to that real URL, then commit and push.

GitHub Actions builds the site automatically on each push to `main`.

## 5. Customize

- `index.qmd`: introduction and homepage
- `experience.qmd`: professional and research experience
- `projects.qmd`: projects and executable R example
- `leadership.qmd`: leadership and technical skills
- `styles.css`: fonts, layout, colors
- `_quarto.yml`: navigation, site title, social links, site URL
- `assets/resume.pdf`: original resume, linked from the navbar

**Privacy:** The provided resume PDF includes your phone number and email address. Anything committed to a public GitHub repository and deployed to Pages is publicly accessible. Replace or remove that PDF if you do not want those details public.

## Updating the website

```bash
git add .
git commit -m "Update portfolio"
git push
```

## Folder structure

```text
.
├── _quarto.yml
├── index.qmd
├── experience.qmd
├── projects.qmd
├── leadership.qmd
├── styles.css
├── assets/
│   └── resume.pdf
├── .github/workflows/publish.yml
├── .gitignore
└── README.md
```
