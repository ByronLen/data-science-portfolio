# data-science-portfolio

A single-page GitHub Pages portfolio presenting Byron's reproducible Palmer Penguins analysis.

- [Live site](https://byronlen.github.io/data-science-portfolio/)
- [Featured project](https://github.com/ByronLen/data-science-project)
- [Portfolio repository](https://github.com/ByronLen/data-science-portfolio)

## Structure

~~~text
data-science-portfolio/
├── README.md
├── _config.yml
├── index.md
├── .gitignore
└── assets/
    └── img/
        ├── 01_measurements_by_species.png
        ├── 02_bill_vs_flipper.png
        └── 03_confusion_matrix.png
~~~

## Publish and maintain

The human owner creates a **public** repository named data-science-portfolio, pushes main, then selects **Settings → Pages → Deploy from a branch → main → / (root)**. The default GitHub Pages Jekyll build uses jekyll-theme-minimal without custom plugins or an Actions workflow.

Edit index.md for content and status; edit _config.yml for the site title and description. Copy regenerated project figures into assets/img/ using the same lowercase filenames. Check numbers against the project README and results/metrics.txt, commit the relevant changes, and push when ready. Once Pages is configured, pushes rebuild the site automatically.

After each deployment, verify every link, all three images, and the layout at a 375px viewport. Update the site status to Live only after verification. Record peer feedback with dates, initials, changes, and actual commit links; update Moodle status only after posting. The current bio and learning reflection are intentionally general; replace them if the author wants a more personal statement.

## Status

| Component | Status |
|---|---|
| Analysis code and README | Complete |
| Two or more visualizations | Complete |
| GitHub Pages site | Live — verified 2026-10-21 |
| Peer feedback and revision | Planned |
| Moodle post | Not posted yet |

The human author independently reran the analysis on 2026-10-21 and confirmed exact reproduction. This is separate from peer feedback. The portfolio repository and GitHub Pages site are live; the deployed site was verified on 2026-10-21.

## AI assistance

An external AI assistant (OpenAI Codex) generated the initial analysis code and project documentation and executed the reported workspace validation. The human author selected the topic, reviewed the code and project README, independently reran the analysis on 2026-10-21, and confirmed that the reported outputs reproduced exactly. The human author retains responsibility for publication and final decisions.

The assistant also prepared this portfolio draft under human direction. The human author confirmed the public name and publication; the bio remains intentionally general. See the [project AI assistance statement](https://github.com/ByronLen/data-science-project/blob/main/README.md#ai-assistance).

## Local validation (2026-10-21)

YAML front matter and theme configuration parse successfully. The source has one content H1, and the theme header adds a site-title H1; all three images have descriptive alt text, the status tables have two columns, and image paths are relative. Copied figures match the original project byte for byte.

A local approximation using Markdown rendering and the Minimal theme's public stylesheet loaded all three figures and showed no horizontal overflow at 375px (document width 375px). The deployed GitHub Pages build was verified on 2026-10-21: it returned HTTP 200, declared UTF-8, loaded the theme stylesheet, and displayed all three images. A final phone check is still recommended.

The GitHub profile, project repository, project README, data page, DOI, portfolio repository, and live site returned HTTP 200. The link checker checked 11 unique targets: seven links and three images, plus the page itself, with zero failures. The all-links-reachable and Pages-build quality gates are met; the mobile layout still needs a final visual check on a real phone.
