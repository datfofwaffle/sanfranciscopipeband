# Prince Charles Pipe Band: website proof of concept

A single-page static site (plain HTML and CSS, no build step). It works on GitHub Pages as is.

## Publish on GitHub Pages

1. On GitHub, create a **public** repository (for example `pcpb-site`). Free GitHub Pages needs a public repo.
2. Upload the **contents** of this folder so that `index.html` sits at the top level of the repo:
   **Add file → Upload files**, drag in `index.html`, `assets/`, `.nojekyll` and `README.md`, then commit.
3. Go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save.
4. After about a minute the site is live at `https://<your-username>.github.io/<repo-name>/`.

## Before showing it around

- **Placeholders.** Search `index.html` for square brackets. These still need real content: Pipe Major and Drum Sergeant names, practice day/time/location, ages and costs, event dates, and the Donate link (`[ADD LINK]`).
- **Not indexed by search engines.** The `<meta name="robots" content="noindex, nofollow">` line in `<head>` keeps this proof of concept out of Google. Delete that line when the band is ready to go live.
- **Images.** The hero is a photo (`golden-gate-hero.jpg`, with a 900px copy for phones). The two band cards still use placeholder illustrations. To swap in a real photo, drop it in `assets/` and change the matching `src="assets/..."` in `index.html`.
- **Photo rights.** Confirm you have permission to use the hero photo, and add a credit in the footer if its license asks for one.
- **Accent color.** The red is one CSS variable, `--accent`, at the top of the `<style>` block.

## Files

- `index.html`: the whole page
- `assets/`: hero photo, illustrations and favicon
- `.nojekyll`: tells GitHub Pages to serve the files as they are
