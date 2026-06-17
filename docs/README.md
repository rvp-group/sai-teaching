# Spatial AI — Course Website

A static course site (plain HTML + CSS, no build step) for the **Spatial AI** module of
*Elective in Artificial Intelligence*. Ready to deploy on GitHub Pages.

## Files

```
index.html              # the whole site (single page, anchored sections)
assets/css/style.css    # all styles; tweak the :root variables at the top to re-theme
figures/                # put images / diagrams / staff photos here
```

## Deploy on GitHub Pages

1. Push this folder to a GitHub repo.
2. **Settings → Pages → Build and deployment → Source: "Deploy from a branch"**, branch `main`, folder `/ (root)`.
3. Site goes live at `https://<user>.github.io/<repo>/`.

No Jekyll needed. (If you later want auto-generated nav or a blog, the natural upgrade is
Jekyll with the **Just the Docs** or **Minimal Mistakes** theme — but plain HTML is simpler
to maintain for a single course page, so I'd stay here unless you outgrow it.)

## Fields to populate (search the HTML for `TODO`)

**Hero / Logistics**
- Academic year, room, day & time of lectures and practicals
- Office hours, communication channel (mailing list / chat)

**Schedule** — for each of the 18 lectures + 5 practicals:
- `Date` — the calendar date
- `Suggested Reading` — paper titles/links (the inspiration page lists 2–3 papers per lecture)
- `Materials` — add an `href` to each `<a class="todo-link">slides</a>` once uploaded.
  As soon as a link has an `href`, it auto-styles as an active blue link (dashed placeholder otherwise).

**Grading** — project deliverables, deadlines, team size, leaderboard rules.

**Staff** — real names, emails, websites, and (optional) photos in `figures/`.
Swap the letter avatar `<div class="person__avatar">L</div>` for `<img src="figures/luca.jpg" ...>` if you prefer photos.

**Resources** — real links for PyTorch3D, NeRFStudio, COLMAP, DreamerV3, reading list.

**Footer** — "Last updated" date.

## Re-theming

Open `assets/css/style.css` and edit the variables under `:root` — `--accent` is the primary
blue, `--week-bg` the lavender week-separator rows (matching your inspiration table). Everything
else derives from those.

## Adding slides

Drop PDFs in a `slides/` folder and point the lecture's link at it, e.g.:

```html
<td class="col-mat"><a class="todo-link" href="slides/lec01-intro.pdf">slides</a></td>
```
