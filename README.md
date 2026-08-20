# Hengjie Liu — personal website

A small Astro-based academic/research website intended for `https://hengjieliu.github.io`.

## What you normally edit

### 1. Homepage sections

The editable content for each homepage section is stored in Markdown under `src/content/sections/`:

- `about.md` — bio, name, role, kicker, and research trajectory
- `skills.md` — skill groups and tags in YAML frontmatter
- `projects.md` — Projects section heading; individual cards remain in `src/content/projects/`
- `publications.md` — ordered publication list and Markdown formatting such as bold author names

`src/pages/index.astro` controls layout and rendering. Change the Markdown files when changing visible page text.

### 2. Projects
Each project is one Markdown file:

- `src/content/projects/musa.md`
- `src/content/projects/dir-revisited.md`
- `src/content/projects/right-prior-dir.md`

To add a new project later, copy one of those files, change the frontmatter and text, and set a new `order` number. The homepage discovers it automatically.

To change a figure, edit only the `image:` line. The image can be:

- a raw GitHub image URL, or
- a local file such as `/images/my-project.png` after placing the image in `public/images/`.

### 3. Publications

Publication citations are stored in `src/content/sections/publications.md`. The source publication list is kept at `docs/aaa_publicationlist.docx`; only the entries under its `PUBLICATION` heading are shown on the website.

### 4. Contact/profile links
Open:

`src/data/site.ts`

GitHub, email, LinkedIn, Google Scholar, and CV are currently included.

### 5. Colors/layout
Open:

`src/styles/global.css`

Most global appearance is controlled by the variables at the top, especially:

```css
--accent: #315f8f;
--max-width: 1080px;
--radius: 18px;
```

## Run locally

```bash
npm install
npm run dev
```

Then open the local URL Astro prints in the terminal (normally `http://localhost:4321`).

## Deploy to GitHub Pages

1. Create a repository named `HengjieLiu.github.io` under the `HengjieLiu` GitHub account.
2. Push this entire folder to its `main` branch.
3. In GitHub: **Settings → Pages → Build and deployment → Source → GitHub Actions**.
4. The included `.github/workflows/deploy.yml` builds and publishes the site after each push.

Because this is a special `<username>.github.io` repository, no Astro `base` path is needed.

## CV

The current PDF CV is stored at `public/HengjieLiu_CV.pdf`. If you replace it with another file, place it in `public/` and update the `cv` path in `src/data/site.ts`.
