# Parker's notes for updating the website:
helpful style notes
https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github
https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
https://mmistakes.github.io/minimal-mistakes/docs/utility-classes/

# splash page layout
Splash page layout (Landing homepage) - _layouts/splash.html </br>
Splash page content (Landing homepage) - index.md
Note: Images should be approximately the same width for proper scaling. Export in lower resolution (< 300dpi) if there are issues with images loading slowly.
Note: Headers will be resized depending on the length of the excerpt

# Modify navigation bar
_data/navigation.yml

# to add additional collections associated with new items in nav bar
update config.yml collections with new permalink

# Install ruby / jekyll / bundler for building and hosting website locally
```
# to install ruby and jekyll with wsl2 running ubuntu 20.04 on windows
# note that the existing ruby version that's packaged with ubuntu has conflicts... here's the workaround
sudo apt-get remove ruby

cd $HOME
sudo apt-get update 
sudo apt-get install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libxml2-dev libxslt1-dev libcurl4-openssl-dev libffi-dev

git clone https://github.com/rbenv/rbenv.git ~/.rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
exec $SHELL

git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
exec $SHELL

rbenv install 3.2.1
rbenv global 3.2.1
ruby -v

gem install jekyll bundler
rbenv rehash

jekyll -v

# install github-pages gem
gem install github-pages
bundle update jekyll

```

# Host website locally (make sure to use http and not https)
```
git clone https://github.com/p4rkerw/p4rkerw.github.io && cd p4rkerw.github.io
bundle add webrick
bundle install
bundle exec jekyll serve
# navigate browser to: http://localhost:4000/
```
Alternatively you can preview individual file markdown builds in Rstudio (just not the entire website all at once)

# Modify font sizes
_sass/minimal-mistakes/_variables.css
splash page intro: type-size-6


# Theme

Built on the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) Jekyll theme by Michael Rose (MIT License, see `LICENSE`).

## Running and publishing the site

Preview locally (WSL):

    PAGES_REPO_NWO=p4rkerw/p4rkerw.github.io bundle exec jekyll serve --livereload --force_polling

then open http://localhost:4000. Publish by committing and running `git push origin master`;
GitHub Pages rebuilds the live site in about a minute.

Where things live:

- People: `_people/*.md` (front matter `status: pi|current|alumni`, `order`, `role`, `now`, `linkedin`, `image`)
- Publications / software: `_publications/*.md`, `_software/*.md`
- News and talks: `_posts/` (talks use `categories: [talks]` plus `venue` and `talk_title`)
- Grants: `_data/grants.yml`; datasets: `_data/datasets.yml`; pre-2023 talk counts: `_data/talks_archive.yml`
- Styling: `assets/css/lab.css`
- Analytics: set `analytics.goatcounter` in `_config.yml` to your GoatCounter code
- A link checker runs on every push and weekly (Actions tab, "Link check")
