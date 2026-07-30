# Carwyn Yeo — Portfolio Site

## How I built this

I designed this site around a chess motif, since I'm a former national chess
player and coach — section labels read like game notation ("The middlegame,"
"Endgame"), and I numbered my work experience as moves in a sequence (1.
Fortis → 2. Handshakes → 3. IRAS) rather than a generic timeline. I built it
as a plain multi-page static site — HTML, CSS, and vanilla JS, no framework
and no build step — and ran it locally with Python's built-in HTTP server to
preview each page before shipping it. I chose a black background with a warm
gold accent, added a subtle grain texture and a drifting glow behind the hero
name so the black doesn't sit flat, and gave cards and nav links a hover
lift/glow so the site doesn't read like a static resume.

## How I deployed it

I pushed the folder to a GitHub repo, then connected that repo to Render as a
Static Site — I left the build command blank and set the publish directory
to the repo root, since there's nothing to compile. Render then gave me a
public `onrender.com` URL and now redeploys automatically every time I push
to `main`.

A static multi-page portfolio site. No build step — just HTML, CSS, and vanilla JS.

## Files

- `index.html` — home page
- `work.html` — experience timeline
- `projects.html` — selected projects
- `about.html` — bio and background
- `contact.html` — contact links
- `styles.css` — all styling (shared across pages)
- `script.js` — scroll-reveal animation (respects reduced-motion)

## Deploy to Render (free static site, public URL)

1. **Push this folder to a GitHub repo.**
   From inside this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/carwynyeo/YOUR-REPO-NAME.git
   git push -u origin main
   ```
   (Create the empty repo on GitHub first at github.com/new.)

2. **Create the site on Render.**
   - Go to [render.com](https://render.com) and sign in (GitHub login is easiest).
   - Click **New +** → **Static Site**.
   - Connect your GitHub account if prompted, then select the repo you just pushed.
   - Settings:
     - **Build Command:** leave blank (nothing to build)
     - **Publish Directory:** `.` (the repo root, since `index.html` lives there)
   - Click **Create Static Site**.

3. **Done.** Render will give you a public URL like
   `https://your-repo-name.onrender.com` within a minute or two.
   Every push to `main` auto-redeploys. Because this is a real multi-page
   site, `https://your-repo-name.onrender.com/work.html` etc. all work
   as direct links too.

4. **Optional — custom domain.** In the Render dashboard for this site,
   go to **Settings → Custom Domains** and follow the instructions to point
   a domain you own at it.

## Editing content later

Each page's content lives directly in its own `.html` file, so you can edit
text without touching the CSS. Colors and type are defined once as CSS
variables at the top of `styles.css` under `:root` if you ever want to
restyle — the whole site currently runs off a black background (`--bg`)
with a warm gold accent (`--gold`).
