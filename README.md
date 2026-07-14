# Portfolio site

Plain-HTML, Jekyll-powered portfolio. No CSS framework — Jekyll only
handles repetition (one template for every project page), not styling.

## Add a new project

1. Create `assets/projects/<slug>/` and drop 10 photos in it.
2. Copy `_projects/example-project.md` to `_projects/<slug>.md`.
3. Edit its front-matter: `title`, `date`, `slug`, and the `photos` list
   (must match your actual filenames).
4. Write the project statement below the `---`.
5. Commit and push. The homepage list and the project page are generated
   automatically — no other file needs to change.

## Deploy on GitHub Pages

1. Push this repo to GitHub.
2. Repo Settings → Pages → Source: deploy from branch `main`, folder `/root`.
3. GitHub builds it with Jekyll automatically (no build step needed on
   your end). Site goes live at `https://<username>.github.io/<repo>/`.

## Run locally (optional, to preview before pushing)

```
gem install bundler jekyll
bundle init
echo 'gem "github-pages", group: :jekyll_plugins' >> Gemfile
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.
