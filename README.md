# Jobcentre Pages
Static marketing and langing pages for BC Jobs, driven by [Jekyll](https://jekyllrb.com/).

### BC examples:
* https://get.bcjobs.ca/1-job-99
* https://get.bcjobs.ca/7-day-trial
* https://get.bcjobs.ca/50-off-month-one

### AB example:
* https://get.albertajobcentre.ca/1-job-99

### NS example:
* https://get.novascotiajobs.ca/1-job-99

# Setup
* Install Git: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
* Clone this repo: `git clone https://github.com/bcjobs/jobcentre-get.git`

## Install Jekyll (macOS)
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

## Start Development Server
* In the project directory, start the Jekyll server: `bundle exec jekyll serve`
* Go to http://localhost:4000 in your browser

## Tutorial: Create a new widget page at https://get.bcjobs.ca/cool-widget
  * Add a file to `sites/bcjobs` folder and name it `cool-widget.html`
  * Add a `permalink` to the top of the page, followed by HTML. For example:
  * The `permalink` specifies what the page URL will be. For example, `bcjobs/cool-widget` means:
    * The URL during development will be http://localhost:4000/bcjobs/cool-widget
    * The URL in production will be https://get.bcjobs.ca/cool-widget
  ```
  ---
  permalink: bcjobs/cool-widget
  ---

  <!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  </head>
  <body>
    <h1>Hello world!</h1>
  </body>
  </html>
  ```
  * Preview the new page at http://localhost:4000/bcjobs/cool-widget

  For more information, visit the official Jekyll site: https://jekyllrb.com/

# Deployment
* Push master branch to GitHub. This will trigger continuous deployment to update the remote site on Netlify.
* Example:
  * Note: we're using `Add cool widget page` commit message below, but make sure to customize your commit messages appropriately.
  ```
  git add .
  git commit -m "Add cool widget page"
  git push
  ```