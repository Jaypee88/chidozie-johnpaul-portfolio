# Nwankwo Chidozie Johnpaul — Portfolio Website

A multi-page personal portfolio site. Plain HTML/CSS/JS — no build step, no framework, so it's easy to edit and free to host.

## File structure

```
portfolio/
├── index.html         Home
├── about.html          About
├── projects.html       Projects
├── experience.html     Experience & Leadership
├── skills.html         Skills
├── community.html      Community & Teaching
├── contact.html        Contact
├── css/
│   └── style.css       All styling (colors, type, layout)
├── js/
│   └── main.js         Mobile nav toggle
└── assets/
    └── images/
        └── profile.jpg Your photo (already in place)
```

## 1. Your profile photo

Already placed at `assets/images/profile.jpg` and wired into the hero section of `index.html`. To swap it later for a different photo, just replace that file with a new one **using the same filename**, or update the `src` in `index.html`:

```html
<img src="assets/images/profile.jpg" alt="Portrait of Nwankwo Chidozie Johnpaul">
```

## 2. Editing your LinkedIn URL (or any other link)

Your LinkedIn and GitHub links appear in the nav-adjacent footer of every page, plus the hero and Contact page. To change them, do a find-and-replace across all `.html` files:

- LinkedIn: search for `https://www.linkedin.com/in/chidozie-nwankwo-b798b4382`
- GitHub: search for `https://github.com/Jaypee88`
- Email: search for `dozienwankwo7@gmail.com`

Most code editors (VS Code, Sublime) have a "Find in Folder" / "Replace All in Files" feature — use that so you don't miss an instance.

## 3. Running it locally

No installation needed. Two options:

**Simplest:** double-click `index.html` and it opens in your browser. (Links between pages will work; a couple of browsers restrict local file access for other features, which is why option 2 is more reliable.)

**More reliable — run a tiny local server:**

```bash
cd portfolio
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

## 4. Pushing it to GitHub

```bash
cd portfolio
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/Jaypee88/YOUR-REPO-NAME.git
git push -u origin main
```

Replace `YOUR-REPO-NAME` with whatever you name the repository (e.g. `portfolio` or `nwankwo-portfolio`).

## 5. Deploying it publicly (GitHub Pages — free)

1. Push the code to GitHub (step 4).
2. On GitHub, go to your repository → **Settings** → **Pages**.
3. Under "Build and deployment," set **Source** to `Deploy from a branch`.
4. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
5. GitHub will give you a live URL, typically `https://Jaypee88.github.io/YOUR-REPO-NAME/`, live within a minute or two.

Any time you push new changes to `main`, the live site updates automatically.

## Notes

- All content is written from what you provided — nothing invented. If your role, dates, or a project's status changes, update the relevant page directly; the copy is plain text inside each `.html` file.
- Colors, fonts and spacing all live in `css/style.css` under the `:root` variables at the top, if you want to adjust the palette later.
