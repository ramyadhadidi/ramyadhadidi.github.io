# ramyadhadidi.github.io

My personal site is built with [Jekyll](https://jekyllrb.com/) on top of the Minimal Mistakes / Academic Pages theme. This document captures everything you need to reproduce the GitHub Pages build locally so changes can be previewed before pushing to `master`.

## Tech stack

- Ruby + Bundler + `github-pages` gem (mirrors the GitHub Pages environment)
- Node.js/npm for the legacy JS bundling scripts (`npm run build:js`)
- SCSS pipeline handled by Jekyll/Minimal Mistakes

## Prerequisites

Install the following on your development machine (macOS instructions assume Homebrew):

1. **Ruby** that matches GitHub Pages (currently 3.3.x). `brew install ruby` or manage via rbenv/asdf.
2. **Bundler**: `gem install bundler` (Bundler 2.5+ recommended).
3. **Node.js 18+**: `brew install node` (needed only if you plan to rebuild/minify custom JS).
4. **GNU make / build essentials** (already available on macOS once Command Line Tools are installed).

> Tip: run `ruby -v`, `bundler -v`, and `node -v` to confirm everything before continuing.

## First-time setup

```bash
git clone git@github.com:ramyadhadidi/ramyadhadidi.github.io.git
cd ramyadhadidi.github.io

# Install Ruby gems (matches GitHub Pages build)
bundle install --path vendor/bundle   # keeps gems out of the system directories

# Capture the resolved gem set so GitHub Pages matches your local env
bundle lock --add-platform ruby
git add Gemfile.lock   # commit whenever the lock file changes

# Install optional Node dependencies for JS bundling
npm install
```

If Bundler warns about missing platforms, you can record the lockfile platform locally with `bundle lock --add-platform ruby`. This keeps your environment aligned with GitHub Pages.

## Running the site locally

Use the default production config plus the development overrides to disable analytics and enable expanded Sass output:

```bash
bundle exec jekyll serve --livereload --config _config.yml,_config.dev.yml
```

The site will be available at `http://localhost:4000/` (as defined in `_config.dev.yml`). `Ctrl+C` stops the server.

## Building for production

```bash
bundle exec jekyll build --config _config.yml
```

The generated site will be written to `_site/`. GitHub Pages performs the same command automatically on every push to `master`.

## JavaScript bundling (optional)

If you edit files under `assets/js`, rebuild the minified bundle before committing:

```bash
npm run build:js   # Uses UglifyJS to regenerate assets/js/main.min.js
```

You can watch for changes with `npm run watch:js` while iterating locally.

## Useful troubleshooting commands

- `bundle exec github-pages versions` – see the exact gem/toolchain versions GitHub Pages expects.
- `bundle update github-pages` – sync to the latest GitHub Pages gem (run sparingly and test).
- `bundle exec jekyll doctor` – catch common configuration pitfalls.

## Credit / references

- Theme foundation: [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)
- Academic Pages starter: https://academicpages.github.io/