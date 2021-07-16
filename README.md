## My Guide

- Font: _sass/_reset.scss
- Font loading: assets/css/academicons.css
- Colors and variable: assets/css/main.scss
- Icons:
    - Icons Drawing: assets/fonts/fontawesome-webfont.svg
    - Icon CSS: _sass/vendor/font-awesome/_icons.scss
    - Icon Drawing: assets/fonts/academicons.svg
    - Icons CSS: assets/css/academicons.css
    - Icon Usage per Class: _sass/vendor/font-awesome/_variables.scss
    - Icon Classes: _sass/vendor/font-awesome/_icons.scss

## To run locally (not on GitHub Pages, to serve on your own computer)
1. Clone the repository and made updates as detailed above
1. Make sure you have ruby-dev, bundler, and nodejs installed: `sudo apt install ruby-dev ruby-bundler nodejs`
1. Run `bundle clean` to clean up the directory (no need to run `--force`)
1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
1. Run `bundle exec jekyll serve` to generate the HTML and serve it from localhost:4000

See more info at https://academicpages.github.io/