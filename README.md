# data-science-portfolio

A single-page GitHub Pages portfolio presenting Byron's reproducible Palmer Penguins analysis.

- [Live site — pending deployment](https://ByronLen.github.io/data-science-portfolio/)
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

After deployment, verify every link, all three images, and the layout at a 375px viewport. Update the site status to Live only after verification. Record peer feedback with dates, initials, changes, and actual commit links; update Moodle status only after posting. Confirm the default student identity and proposed first-person learning reflection before publication.

## Status

| Component | Status |
|---|---|
| Analysis code and README | Complete |
| Two or more visualizations | Complete |
| GitHub Pages site | Pending deployment |
| Peer feedback and revision | Planned |
| Moodle post | Not posted yet |

The human author independently reran the analysis on 2026-10-21 and confirmed exact reproduction. This is separate from peer feedback. This portfolio has not been deployed or pushed by the assistant.

## AI assistance

An external AI assistant (OpenAI Codex) generated the initial analysis code and project documentation and executed the reported workspace validation. The human author selected the topic, reviewed the code and project README, independently reran the analysis on 2026-10-21, and confirmed that the reported outputs reproduced exactly. The human author retains responsibility for publication and final decisions.

The assistant also prepared this portfolio draft under human direction. Human review of the portfolio's personal statements and final publication remains pending. See the [project AI assistance statement](https://github.com/ByronLen/data-science-project/blob/main/README.md#ai-assistance).
