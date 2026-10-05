# Personal Academic Website (photo edition)

A single-page site with About, Research, Projects, Publications, and Contact tabs. It's built around pictures: a hero banner, a field photo gallery, photo cards, figure thumbnails for papers, and a full-screen viewer with captions for every image.

## Deploy on GitHub Pages

1. Create a public repo named **`yourusername.github.io`**.
2. Upload `index.html` and the whole `images/` folder.
3. Go to **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. After a minute, your site is live at `https://yourusername.github.io`.

## Add your own content and photos

All content lives in **one place**: the `SITE` object near the bottom of `index.html`. You don't need to touch any HTML.

- **Swap a photo:** put your picture in `images/` with the same file name (e.g. `images/hero.jpg`), or change the path in `SITE`.
- **Add gallery photos:** add a line like `{ img: "images/gallery/my-photo.jpg", caption: "..." }`. Tall, wide, or square photos all fit.
- **Add a project or paper:** copy an existing entry and edit it. For projects, `cover` is the card photo; `img`, `text` (abstract), `stats`, `tags` and `links` appear in the pop-up when the card is clicked.
- **Photos for papers:** a figure or graphical abstract works well. Leave out `img` and the entry shows as text only.
- **Missing images** are skipped automatically, so nothing breaks while you're filling things in.

### Photo tips
- Resize photos to about **1600–2000 px wide** and save as JPG (around 200–400 KB each) so the site loads fast. On a Mac, Preview → Tools → Adjust Size does this.
- Use lowercase, dash-separated file names (`summer-field-2026.jpg`). GitHub Pages treats `Photo.JPG` and `photo.jpg` as different files.

## Add your paper PDFs
Put PDFs in the `papers/` folder and link them in a publication's `links`, e.g. `PDF: "papers/li-2026-genetic-diversity.pdf"`. Only post versions your publisher allows (usually the accepted manuscript). Each file must be under 100 MB.

## Change the colors
Edit `--accent` at the top of the `<style>` block. Dark mode adjusts automatically.

## License

See `LICENSE` (code) and `LICENSE-CONTENT.md` (text, figures, photos). In short: the **code** is MIT, the **written content and your own figures** are CC BY 4.0, and the **photos** belong to their photographers and are not covered by either license. You can change any of these: for example, use "All rights reserved" for the text if you don't want it reused.
