# chrischow1.github.io

Academic portfolio site built with Jekyll (al-folio-inspired).

## Customize

- Update profile details in `_config.yml`.
- Edit content in `_data/publications.yml`, `_data/projects.yml`, `_data/experience.yml`.
- Replace `assets/img/headshot.svg` with your photo.
- Replace `assets/resume.pdf` with your resume PDF.
- Tweak styling in `assets/css/main.css`.

## GitHub Pages

### User site
- Repo name: `yourname.github.io`
- Set `baseurl: ""` in `_config.yml` (already default).

### Project site
- Repo name: any name, publish at `https://yourname.github.io/repo-name/`
- Set `baseurl: "/repo-name"` in `_config.yml`.

## Local preview (optional)

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.
