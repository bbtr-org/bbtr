# BBTR

Source code for [bbtr.fr](https://bbtr.fr).

Relevant documentation:
- The Static Site Generator: [MkDocs](https://www.mkdocs.org/)
- Our theme is [Material for Mkdocs](https://squidfunk.github.io/mkdocs-material/)
    - (note that the theme does almost more than the base framework in terms
      of what the website does, how it works etc. If you need anything, it's
      most likely there)
    - See the [config](mkdocs.yml) page, there are some comments here for
      some specific features
- [Cloudflare pages](https://developers.cloudflare.com/pages/)
    - In particular, if you submit a PR, you should get a link to a domain
      where you can preview your changes

## Local dev

```console
(venv) $ pip install -r requirements.txt
(venv) $ mkdocs serve
(venv) $ # Build locally with:
(venv) $ mkdocs build
```

## Deployment

Everything is setup so that the site is uploaded when you merge the main branch.

## Updating the dependencies

Using `pip-compile` for package `pip-tools` (if you don't have it, `pipx` is a great
option):
```
(venv) $ pip-compile --upgrade requirements.in
```
Commit the resulting `requirements.txt`
