# Rollo Tully's super amazing website

The original Bootstrap 3 styling, with a homepage bio, three featured projects,
a full Projects page and a gallery for each project. GitHub Pages' Jekyll build discovers photos and videos automatically;
there is no image list to maintain and no browser API request to GitHub.

## Homepage bio and project lists

Edit `_data/bio.yml` to change the name, short blurb and headshot image path.
The initial blurb and headshot are placeholders. Add your photo under `Images/`
and point `headshot` at it, for example `/Images/headshot.jpg`.

The homepage shows only the first three entries in `_data/projects.yml`, below
the bio. Reorder that file to change which projects appear. `projects.html`
shows the complete list with the same grid, without the bio. Both pages use
`_layouts/project-list.html`, so their project cards stay consistent.

## Adding photos and videos

1. Put your photos and videos in the project's folder below, or use **Add file → Upload
   files** inside that folder on GitHub.
2. Commit and push to the branch used by GitHub Pages.
3. Once the Pages build finishes, the photos and videos appear in the gallery.

| Project | Media folder |
| --- | --- |
| Hecate | `Images/Hecate/` |
| Fortis | `Images/BMFA/` |
| SwarmCut | `Images/SwarmCut/` |
| Halcyon | `Images/Halcyon/` |
| Meteosat Image reception | `Images/Sat decoding/` |
| Highspeed Photography | `Images/Highspeed Photography/` |
| X-Band SAR | `Images/X-Band SAR/` |

Images: JPG/JPEG, PNG, GIF, WebP, AVIF and SVG. Videos: MP4 and WebM.
Uppercase extensions and subfolders work too. Photos and videos are sorted
together by their full filename; use `01-front.jpg`, `02-flight.mp4` to control
the order.

Videos have native playback controls and play inline on phones. MP4 encoded as
H.264 with AAC audio is a widely compatible choice; playback
depends on the browser's codec support. Convert MOV/AVI files before uploading.
See [MDN's video codec guide](https://developer.mozilla.org/en-US/docs/Web/Media/Guides/Formats/Video_codecs).

The homepage uses the first picture in the folder. Four existing projects have
a preferred `cover` filename in `_data/projects.yml`; change or remove it if you
want a different cover. If that file is removed, the first remaining picture is
used instead. Homepage covers use still images, so add a JPG/PNG alongside a video
if you want a cover picture. Empty galleries show a labelled placeholder until
you add a photo or video.

## GitHub Pages setup

These are Jekyll templates. In the repository's **Settings → Pages**, use
**Deploy from a branch**, select **main** and **/ (root)**, then save. Do not add
a `.nojekyll` file. A custom Actions deployment must build with Jekyll before
uploading the site. The repository settings have not been changed by this patch.

For a local preview, install Jekyll and run `jekyll serve` from this folder.
Opening the source `index.html` directly will show template code instead.

Navigation and gallery back links lead to the full Projects page.
The existing Munro Map content is retained.

Reference: [GitHub Pages and Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll).
