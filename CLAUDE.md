# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the GitHub Pages website for the Urban3D Challenge - an academic competition focused on large-scale 3D point cloud analysis for urban scenes understanding. The site documents challenge editions from 2021, 2022, and 2023.

**Live site:** https://urban3dchallenge.github.io/

**Repository:** https://github.com/Urban3DChallenge/Urban3DChallenge.github.io

## Architecture

### Single-Page Application Structure
- `index.html` - Main landing page for the 2023 challenge edition
- `2021/index.html` - 2021 challenge edition page
- `2022/index.html` - 2022 challenge edition page

Each year's page is self-contained with embedded styles and references shared assets from the `2023/` folder.

### Asset Organization
```
2023/
├── css/
│   ├── bootstrap.min.css    # Bootstrap framework
│   └── main.css             # Custom styles for all pages
└── img/
    ├── people/              # Speaker and organizer photos
    ├── banner.jpg           # Hero banner
    └── *.png                # Sponsor and logo assets
```

### Key Page Sections (index.html)
- `#intro` - Introduction and challenge overview
- `#calls` - Call for Contributions with challenge tracks
- `#dates` - Important dates and schedule
- `#speakers` - Invited speakers with collapsible bios
- `#organizers` - Organizer list with photos
- `#sponsors` - Sponsor logos
- `.u3d-institutions` - Participating institutions scrolling banner
- `#contact` - Contact information section
- `#footer` - ARL sponsorship disclaimer

### Navigation
Year navigation header (`#year-header`) allows switching between editions. Main navbar (`#navbar-main`) contains anchor links to sections.

## Repository Account

**Important:** This repository uses a dedicated GitHub account for the Urban3D Challenge, separate from personal accounts:
- **GitHub username:** `Urban3DChallenge`
- **Email:** `gfkdhuqingyong@gmail.com`

When committing or pushing changes, use this account's credentials.

## Development

### Local Preview
```bash
# Serve the site locally (Python 3)
python -m http.server 8000

# Or with Python 2
python -m SimpleHTTPServer 8000
```

Then open http://localhost:8000

### Git Workflow
This repository uses `master` locally but pushes to `main` on remote:
```bash
git push origin HEAD:main
```

### Adding Images
- Person photos go in `2023/img/people/`
- Use consistent naming (e.g., `firstname-lastname.jpg`)
- Reference as `./2023/img/people/filename.jpg` from root index.html

### Styling Notes
- Bootstrap 3.x provides base styling
- `main.css` contains custom overrides and challenge-specific styles
- Inline `<style>` block in index.html for year-header and institutions banner
- Institutions banner uses CSS animations for continuous scrolling

## Important Content References

### CodaBench Migration Notice
The challenge platform migrated from CodaLab to CodaBench. The alert banner near `#intro` section must remain prominent with link:
- URL: https://www.codabench.org/competitions/15137/

### Contact Information
- Qingyong Hu is the corresponding organizer
- Email: huqingyong15@outlook.com
- Photo: `2023/img/qingyong-hu-contact.jpg`

### Challenge Links
- SensatUrban dataset: http://point-cloud-analysis.cs.ox.ac.uk/
- GitHub: https://github.com/QingyongHu/SensatUrban
- Old CodaLab links remain in `#calls` section for historical reference
