# Build from Gem package

## Prerequisites
Jekyll requires the following:

* [Ruby version 2.5.0 or higher](https://www.ruby-lang.org/en/downloads/)
* RubyGems
* GCC and Make

### Install Jekyll & Bundler
```bash
gem install bundler jekyll
```

## Create new jekyll site
```bash
jekyll new mysite

cd mysite
bundle config path 'vendor/bundle'
```

## Update `Gemfile` & `_config.yml`
Replace the contents of Gemfile as follows:

```ruby
source "https://rubygems.org"

gem "jekyll", "~> 3.9"
gem "jekyll-professional-resume", "~> 0.0.1"

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-sitemap", "~> 1.3", '< 1.4'
  gem "jekyll-seo-tag", "~> 2.6"
  gem "kramdown-parser-gfm", "~> 1.1.0"
  gem "webrick", "~> 1.7.0"
end
```

For `_config.yml` file, 
```yml
title: Matthew's Live Curriculum Vitae
profile_img: assets/img/profile.webp
icon_img: assets/img/icon.webp

name: "Matthew Hatami"
job: "〈PhD Student | Aspiring Geospatial Data Science〉"

phone_number: 039 331-253 8654
address: Columbia (SC), USA
email: mhatami@sc.edu
linkedin_username: matthewHatami
github_username: matthewHatami
instagram_username: matthew.scholar
twitter_username: matthewhatami1
facebook_username: facebook

theme: jekyll-professional-resume

exclude:
  - _posts/
  - resources/
  - vendor/
```

## Run site locally

To test locally, run the following:

```
bundle install
bundle exec jekyll serve
```

Now open [http://localhost:4000](http://localhost:4000) in your browser.
<br></br>