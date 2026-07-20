# lucasreed.io

Personal hub site for Lucas Reed — rail engineer, sci-fi author, musician, and astrophotographer.

## Stack

- Single-file HTML/CSS/JS (no build step, no dependencies)
- Deployed via GitHub Pages
- Domain: lucasreed.io (point to GitHub Pages via Namecheap DNS)

## Deploy

```bash
# First time setup
git init
git add .
git commit -m "Initial build"
gh repo create Ldreed1/lucasreed-io --public --push --source=.

# Enable GitHub Pages in repo settings:
# Settings → Pages → Source: Deploy from branch → Branch: main → / (root)

# After Pages is enabled, all future deploys:
git add -A && git commit -m "update" && git push
```

## Domain Setup (Namecheap)

After GitHub Pages is live at `Ldreed1.github.io/lucasreed-io`:

1. Log into Namecheap as Ldreed1
2. Buy `lucasreed.io` (~$35-45/yr)
3. Go to Domain → Advanced DNS and add:

| Type  | Host | Value                    | TTL  |
|-------|------|--------------------------|------|
| A     | @    | 185.199.108.153          | Auto |
| A     | @    | 185.199.109.153          | Auto |
| A     | @    | 185.199.110.153          | Auto |
| A     | @    | 185.199.111.153          | Auto |
| CNAME | www  | Ldreed1.github.io        | Auto |

4. In GitHub repo → Settings → Pages → Custom domain → enter `lucasreed.io`
5. Check "Enforce HTTPS" once it propagates (~10-30 min)

## Adding Astrophotography Images

Replace the placeholder `gallery-item` divs in the Space section with:

```html
<div class="gallery-item">
  <img src="images/your-photo.jpg" alt="Description of object" />
</div>
```

Put images in an `images/` folder alongside index.html.

## Updating Content

All content is in `index.html`. Key sections to update before launch:

- [ ] LinkedIn URL (currently placeholder) — update in Contact section
- [ ] Astrophotography images — replace 6 placeholder tiles in Space section
- [ ] Music links — add Spotify/DistroKid links when first release is out
- [ ] Book cover art — replace the CSS gradient placeholder with real cover image
- [ ] Engineering section — adjust card copy as desired

## Formspree

Contact form and Signal email list both submit to `https://formspree.io/f/xqeypwqz`
(same form used on lucasreedbooks.com). Check submissions at formspree.io.

## lucasreedbooks.com

After lucasreed.io is live, update the Ldreed1 GitHub Pages repo (lucasreedbooks) to
add a redirect or a prominent link back to lucasreed.io as the primary hub.
