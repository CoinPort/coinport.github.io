source "https://rubygems.org"

# Core Jekyll - GitHub Pages compatible version
gem "jekyll", "~> 3.9.5"

# GitHub Pages - ensures all dependencies match GitHub's environment
gem "github-pages", "~> 231", group: :jekyll_plugins

# Theme
gem "minima", "~> 2.5"

# Jekyll Plugins
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.17"
  gem "jekyll-seo-tag", "~> 2.8"
  gem "jekyll-sitemap", "~> 1.4"
  gem "jekyll-titles-from-headings"
  gem "jekyll-redirect-from", "~> 0.16"
  gem "jekyll-include-cache", "~> 0.2"
end

# Required for Ruby 3.0+
gem "webrick", "~> 1.8"

# Markdown parser
gem "kramdown-parser-gfm", "~> 1.1"

# Security - minimum safe versions
gem "nokogiri", ">= 1.18.7"
gem "rexml", ">= 3.3.6"

# HTTP parser fix
gem "http_parser.rb", "~> 0.8.0"

# Platform-specific gems for Windows
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Windows directory monitor
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]
