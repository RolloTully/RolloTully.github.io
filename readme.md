# Rollo Tully's super amazing website

The original Bootstrap 3 styling, with projects on the homepage and a photo page
for each project. GitHub Pages' Jekyll build discovers the pictures automatically;
there is no image list to maintain and no browser API request to GitHub.

## Adding pictures

1. Put your pictures in the project's folder below, or use **Add file → Upload
   files** inside that folder on GitHub.
2. Commit and push to the branch used by GitHub Pages.
3. Once the Pages build finishes, the pictures appear in the gallery.

| Project | Picture folder |
| --- | --- |
| Hecate | `Images/Hecate/` |
| Fortis | `Images/BMFA/` |
| SwarmCut | `Images/SwarmCut/` |
| Halcyon | `Images/Halcyon/` |
| Meteosat Image reception | `Images/Sat decoding/` |
| Highspeed Photography | `Images/Highspeed Photography/` |
| CAMO GAN | `Images/CAMO GAN/` |
| Boggle Engine | `Images/Boggle Engine/` |
| X-Band SAR | `Images/X-Band SAR/` |

JPG/JPEG, PNG, GIF, WebP, AVIF and SVG are supported, including uppercase file
extensions. Subfolders are included. Pictures are sorted by their full filename;
use names such as `01-front.jpg`, `02-build.jpg` to control the order.

The homepage uses the first picture in the folder. Four existing projects have
a preferred `cover` filename in `_data/projects.yml`; change or remove it if you
want a different cover. If that file is removed, the first remaining picture is
used instead. Empty galleries show a labelled placeholder until you add a photo.

## GitHub Pages setup

These are Jekyll templates. In the repository's **Settings → Pages**, use
**Deploy from a branch**, select **main** and **/ (root)**, then save. Do not add
a `.nojekyll` file. A custom Actions deployment must build with Jekyll before
uploading the site. The repository settings have not been changed by this patch.

For a local preview, install Jekyll and run `jekyll serve` from this folder.
Opening the source `index.html` directly will show template code instead.

The old `projects.html` address sends visitors to the homepage's Projects section.
The existing Skills, Tools and Munro Map content is otherwise retained.

Reference: [GitHub Pages and Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll).
