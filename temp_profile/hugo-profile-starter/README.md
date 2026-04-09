# Gilbert Onyenwezi Portfolio Starter (hugo-profile)

This starter is tailored to the `hugo-profile` theme.

## Setup

1. Create a new Hugo site with YAML config.
2. Add the theme:
   - `git submodule add https://github.com/gurusabarish/hugo-profile.git themes/hugo-profile`
3. Copy these files into the site root.
4. Run `hugo server`.

## Included

- `hugo.yaml` with homepage sections configured
- `content/` pages for About, Experience, Education, Contact, and Projects
- `static/files/resume.pdf`
- placeholder SVG images in `static/images/`
- `netlify.toml`

## Important

If the theme errors on pages without tags, update:

```go
{{ with .Params.tags }}{{ delimit . ", " }}{{ end }}
```

inside `themes/hugo-profile/layouts/_default/single.html`.
