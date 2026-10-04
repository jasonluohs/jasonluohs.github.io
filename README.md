# jasonluohs.github.io

Luo Hongsen's personal website — pure static HTML/CSS, no build step, no external
dependencies. Hosted on GitHub Pages at <https://jasonluohs.github.io>.

## Pages

| File            | Page      | Status                        |
| --------------- | --------- | ----------------------------- |
| `index.html`    | Home      | placeholder content ready     |
| `about.html`    | About     | placeholder content ready     |
| `cv.html`       | CV        | content mirrors `resume.tex`  |
| `projects.html` | Projects  | 4 case-study skeletons        |
| `research.html` | Research  | 3 questions + timeline        |
| `notes.html`    | Notes     | intentionally empty (预留)     |
| `contact.html`  | Contact   | email + GitHub live           |

## Preview locally

```bash
cd jasonluohs.github.io
python3 -m http.server 8000
# then open http://localhost:8000 in a browser
```

Opening `index.html` directly in a file manager also works (all links are `.html`).

## Deploy to GitHub Pages

1. On GitHub, create a **public** repository named exactly `jasonluohs.github.io`
   under the `jasonluohs` account (do not initialize it with a README).
2. Then:

```bash
cd jasonluohs.github.io
git init
git add -A
git commit -m "Initial version of personal website"
git branch -M main
git remote add origin git@github.com:jasonluohs/jasonluohs.github.io.git
# or HTTPS: https://github.com/jasonluohs/jasonluohs.github.io.git
git push -u origin main
```

3. In the repo: Settings → Pages → Source: *Deploy from a branch* → Branch: `main` / `(root)`.
4. Wait ~1 minute, then visit <https://jasonluohs.github.io>.

## How to fill in your content

- Search the HTML for `TODO` — every spot that needs your real content is marked
  with a Chinese comment explaining what to put there.
- Photos: drop images into `assets/img/` with the filenames shown in the dashed
  placeholder boxes (e.g. `robogame-1.jpg`), then replace the `<div class="ph">`
  box with `<img src="assets/img/robogame-1.jpg" style="width:100%;border-radius:5px;">`.
- CV PDF: compile `resume.tex`, save as `assets/cv.pdf`, and uncomment the
  download link in `cv.html`.
- Colors / fonts: all in one place at the top of `assets/css/style.css` (`:root`).
