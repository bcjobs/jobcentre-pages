# Setup (macOS)
* Update Homebrew: `brew update`
* Use Ruby version manager
  * Install rbenv if it isn't installed: `brew install rbenv`
  * Upgrade rbenv if it's already installed: `brew upgrade rbenv`
* Setup rbenv integration to your shell
  * `rbenv init`
* Install and use Ruby version 2.5.3
  * `rbenv install 2.5.3`
  * `rbenv global 2.5.3`
* Install Jekyll and bundler gems
  * `gem install jekyll bundler`
* Clone this repo
* `cd` into this project folder
* Install gems
  * `bundle install`

# Development
* In the project directly, start the Jekyll server: `bundle exec jekyll serve`
* Go to http://localhost:4000

# Deployment
* Push to master branch on GitHub. This will trigger continuous deployment to update the remote site on Netlify.