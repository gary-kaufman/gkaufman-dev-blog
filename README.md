# gkaufman-dev-blog

This project uses [MkDocs](https://www.mkdocs.org/) and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) to produce a static site for my occasional blog post. The [Setting up a blog](https://squidfunk.github.io/mkdocs-material/setup/setting-up-a-blog/) article by Material for MkDocs has been the most helpful in working on this project.

## Required Packages

- mkdocs
- mkdocs-material

## Local Development

To work with my blog locally, I first install `mkdocs` with the following command.
```commandline
pip install mkdocs mkdocs-material
```

Then inside the source folder I run `mkdocs serve` to inspect my progress in a web browser.

## Deployment

I used the command `mkdocs gh-deploy --force` to deploy directly to GitHub pages per the MkDocs documentation.
