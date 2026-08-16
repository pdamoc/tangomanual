# frozen_string_literal: true

source "https://rubygems.org"

# This site is built and deployed by .github/workflows/pages.yml rather than by
# the classic GitHub Pages builder, so we track Jekyll directly instead of the
# `github-pages` gem (which is still pinned to Jekyll 3.10).
gem "jekyll", "~> 4.4"
gem "jekyll-theme-primer", "~> 0.6"

group :jekyll_plugins do
  gem "jekyll-redirect-from"
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
  gem "jemoji"

  # GitHub Pages enabled these implicitly. The site depends on all of them:
  #   default-layout        -> most pages declare no `layout:` of their own
  #   optional-front-matter -> e.g. README.md, missions/form-template.md
  #   relative-links        -> [text](page.md) links in index.md, v1/index.md
  #   titles-from-headings  -> pages with no `title:` in front matter
  gem "jekyll-default-layout"
  gem "jekyll-optional-front-matter"
  gem "jekyll-readme-index"
  gem "jekyll-relative-links"
  gem "jekyll-titles-from-headings"
end

# jekyll-theme-primer pulls in jekyll-github-metadata -> octokit -> faraday,
# which prints a notice at build time unless the retry middleware is present.
gem "faraday-retry"

# Formerly default gems, unbundled from newer Ruby releases.
gem "base64"
gem "bigdecimal"
gem "csv"
gem "logger"
gem "ostruct"
gem "webrick" # required by `jekyll serve`
