# Personal website

Source for [martinezcolanai.github.io](https://martinezcolanai.github.io), the
academic homepage of Andrés Ignacio Martínez Colán.

Built with [Jekyll](https://jekyllrb.com/) and published automatically by
GitHub Pages on every push to `main`.

## Updating content

See [CONTENT-GUIDE.md](CONTENT-GUIDE.md) — it covers adding publications,
editing the home page, and replacing the portrait, all from github.com without
installing anything.

## Running locally (optional)

Requires Ruby with the DevKit.

```
bundle install
bundle exec jekyll serve
```

The site is then served at <http://localhost:4000>.

## Layout

| Path              | Purpose                                        |
| ----------------- | ---------------------------------------------- |
| `index.html`      | The single-page home, research and publications |
| `_publications/`  | One Markdown file per publication               |
| `_layouts/`       | Page templates                                 |
| `_includes/`      | Head and sidebar partials                      |
| `assets/css/`     | Styles                                          |
| `assets/img/`     | Images                                          |
