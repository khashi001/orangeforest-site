source "https://rubygems.org"

# GitHub Pages用の設定（github-pagesが全ての依存関係を管理）
gem "github-pages", group: :jekyll_plugins

# Jekyll プラグイン（github-pagesに含まれているものを明示的に指定）
group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
end

# Windows と JRuby 用
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Windows 用
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# JRuby 用
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]