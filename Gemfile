source "https://rubygems.org"

gem "jekyll", ">= 3.8.5"
# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
# gem "github-pages", group: :jekyll_plugins

# This is the default theme for new Jekyll sites. You may change this to anything you like.
# gem "minima", "~> 2.5"
# gem "jekyll-theme-clean-blog"

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-paginate", "~> 1.1.0"
  gem "jekyll-sitemap"
end


# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
## gem "wdm", ">= 0.1.1" if Gem.win_platform? # FAUR REMOVED

# Fix: 'require' bundle exec jekyll serve: cannot load such file
# https://stackoverflow.com/questions/65989040/bundle-exec-jekyll-serve-cannot-load-such-file
# https://github.com/jekyll/jekyll/issues/8523
gem "webrick"