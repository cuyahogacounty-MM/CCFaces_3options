# Publishing on GitHub Pages

This site is plain HTML/CSS/JS, so GitHub Pages can host it for free with no
build step. You need a **public** repository (GitHub Pages on the free plan
requires the repo to be public).

## One-time setup

1. Create a new repository on GitHub (e.g. `faces-of-cuyahoga`), set it to
   **Public**, and create it.
2. Upload these files. Two ways:
   - **Web upload:** on the repo page, choose *Add file → Upload files*, then
     drag in `index.html`, the `photos` folder, the `hiring` folder, and the
     `.md` files. Commit.
   - **Git:** clone the repo, copy these files in, then
     `git add . && git commit -m "Add prototype" && git push`.
3. Go to **Settings → Pages**.
4. Under *Build and deployment*, set **Source** to *Deploy from a branch*.
5. Choose branch **main** and folder **/ (root)**. Save.
6. Wait a minute, refresh the Pages settings screen, and the public URL
   appears at the top.

## Your URLs

- Employee grid: `https://YOURNAME.github.io/REPO-NAME/`
- Hiring graphic: `https://YOURNAME.github.io/REPO-NAME/hiring/`

## Updating it later

Edit the files and commit again (or re-upload). GitHub Pages redeploys
automatically within a minute or two.

## A note on the photos

`index.html` references images by relative path (`photos/kelly-marton.jpg`,
etc.). The `photos` folder must stay next to `index.html` with the same
filenames, or those cards fall back to a placeholder. Don't rename the files.

## A note on privacy

These are real county employees. Names and job titles are public record, but
the **published site is public** — anyone can view it and the photos. Make
sure HR has cleared each photo for public use before publishing. To hold a
person back without breaking the layout, set their `photo` to `""` in
`index.html` (see CONTENT.md) and an initials placeholder shows instead.
