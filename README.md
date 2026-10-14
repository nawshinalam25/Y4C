# Integrated Approach for Strategic Mangrove Restoration — Project Website

A static website for the Aqua Lead mangrove-restoration project, funded by
**Youth4Climate 2025** (UNDP & Government of Italy) under the *Nature for
Climate Action* track, with technical support from Bangladesh Maritime
University.

Rebuilt from scratch in the official Y4C 2025 brand system (Barlow /
Barlow Condensed type, Y4C blue/green/yellow/light-blue palette, and the
project's "Nature for Climate Action" orange + swirl-pattern accent),
using real project assets throughout — logos, team photos, CVs, event
photos and blog content.

## Pages

| Page | File |
|---|---|
| Home (slideshow, approach, mission/blog/event teasers) | `index.html` |
| What We Do (4-phase pipeline, study area, deliverables, progress) | `what-we-do.html` |
| Our Mission (mission, vision, 4 objectives, SDGs) | `mission.html` |
| Our Team (5 profiles with CV downloads) | `team.html` |
| Events (upcoming / past, incl. Youth4Climate Flagship Event 2025) | `events.html` |
| Blogs (listing by category + 4 full posts) | `blogs/index.html` and `blogs/blog-0*.html` |
| Gallery (Brasília trip + Flagship Event photos) | `gallery.html` |
| Feedback (public feedback form) | `feedback.html` |

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `aqua-lead-mangrove-restoration`).
2. Push this entire folder to the repository's `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Rebuild project website in Y4C 2025 brand system"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. In the repo settings, go to **Settings → Pages**, set **Source** to
   `Deploy from a branch`, branch `main`, folder `/ (root)`, and save.
4. Your site will be live at `https://<your-username>.github.io/<repo-name>/`
   within a few minutes. Once it's live, add that URL to the "Project
   website" line on the Feedback page and anywhere else you'd like it shown.

No build step is required — this is plain HTML/CSS/JS.

## Videos

Both project videos are embedded as **unlisted YouTube videos** rather than
hosted as files in the repo — this keeps the repo small and avoids GitHub's
100 MB file-size limit entirely:

- **Home page** ("About our project" section, `index.html`) embeds
  `youtu.be/zrw7DQVnRCE`.
- **"From the Sundarbans to Brasília" blog post**
  (`blogs/blog-04-journey-to-brasilia.html`) embeds the YouTube Short
  `youtube.com/shorts/UpVYibaSVi0`.

Being "unlisted" only hides a video from YouTube search and your channel —
it does **not** block embedding. Anyone who opens the website can watch it
inline, with no separate link needed, exactly as embedded here. If you ever
swap in different videos, update the video ID in the `src="https://www.
youtube.com/embed/<id>"` attribute in each of those two files.

## Things that still need your input

- **Feedback form delivery.** The form on `feedback.html` posts to
  [FormSubmit.co](https://formsubmit.co), a free service that emails form
  submissions straight to `aqualead.alm@gmail.com` with no backend or
  signup required. **The first real submission will trigger a one-time
  confirmation email from FormSubmit to that inbox — you must click the
  confirmation link before submissions start arriving.** If you'd rather
  not use a third-party relay, swap the form's `action` for a service like
  Formspree, or a Google Form embed.
- **Blog comments & a posting form.** GitHub Pages is a static host, so it
  can't run a real backend for posting blog entries or hosting public
  comments. Each post page has a `.comments-box` reserved for this — the
  common no-backend fix is embedding
  [Giscus](https://giscus.app) (turns GitHub Discussions on this repo into
  a comment widget) once the repo is public. New posts, for now, are added
  by the team directly as new HTML files following the existing posts as a
  template.
- **Interactive study-area map.** `what-we-do.html` currently shows an
  illustrative, non-geographic sketch map (coordinates intentionally
  withheld to protect site/community privacy, per the guideline). If you'd
  like a real interactive map, the cleanest static-site option is a
  [Leaflet.js](https://leafletjs.com/) embed using only approximate,
  non-sensitive coordinates.
- **Team designations.** The role titles and responsibilities on
  `team.html` are drafted to match each person's CV/role in the project —
  double-check and edit the bullet points in `team.html` if anything needs
  correcting.
- **Video embeds.** See the "Videos" section above — double-check both
  embeds play correctly once the site is live, since unlisted-video
  embedding behaviour is set per-video in YouTube Studio.

## Folder structure

```
y4c-site/
├── index.html, what-we-do.html, mission.html, team.html,
│   events.html, gallery.html, feedback.html
├── blogs/
│   ├── index.html
│   └── blog-01-coastal-resilience.html … blog-04-journey-to-brasilia.html
└── assets/
    ├── css/style.css      — full Y4C 2025 design system
    ├── js/main.js          — nav toggle, slideshow, footer year
    ├── img/brand/          — Y4C + Aqua Lead + BMU logos, patterns
    ├── img/slides/         — home-page slideshow images
    ├── img/team/           — team headshots
    ├── img/events/         — certificate photo
    ├── img/gallery/        — Brasília trip + Flagship Event photos
    └── cv/                 — team CVs (PDF)
```
