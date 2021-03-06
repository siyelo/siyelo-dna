---
---
# Siyelo DNA - tech setup for the site

Siyelo DNA is a web site that describes how Siyelo works and why. The source lives on github and is auto-published on [http://dna.siyelo.com](http://dna.siyelo.com) every time a change is pushed.

Below are instructions for how to set up a local development environment. Useful for when you want to make many changes and test locally before pushing to github. See [How to clone](http://dna.siyelo.com/docs/how-to-copy.html) for more options on how to clone the Siyelo model.


## 1. Install GIT

Here's [how to install GIT](http://git-scm.com/book/en/v2/Getting-Started-Installing-Git). 

## 2. Clone the repo

Tell git to download the siyelo-dna source:

    git clone https://github.com/siyelo/dna.git
    cd dna

You should now have the whole thing, including the README.md file that you are reading right now!

The web site source files are under _docs, have a look! They are written using [textile](http://redcloth.org/textile) (a simpler format than html). When you push to github, it will automatically convert the pages to static html and build the site http://dna.siyelo.com. 

## 3. Install Jekyll and related tools

To test the site locally, you need to install jekyll (the tool that github uses to generate sites), which in turn relies on some Ruby stuff. But you can do all easily via Ruby bundler, like this:

First install Ruby if you don't already have it, for example via [homebrew](http://brew.sh).

    brew install ruby

Then install the Ruby Bundler gem, if you don't already have it.

    gem install bundler

Next, tell the bundler to install all the gems needed (jekyll, github-pages, etc). They are listed in Gemfile in case you are curious.

  bundle install  

Congrats! You got the stuff you need. You should now be ready to....

## 4. Run the site locally!

Tell Jekyll to generate the site and serve it up:

    jekyll serve

Or if you are lazy you can use the run script (which just does jekyll serve)

That's it, your local copy of the Siyelo DNA site should be up and running on
[http://localhost:4000](http://localhost:4000)

Every time you edit a source doc (under _docs) it will update the site automatically.

## Development

Use topic branches off of `master`. Use pull requests.

## Deployment

To deploy to Github pages, merge the `master` branch into `gh-pages`. More info on this here: http://jekyllrb.com/docs/github-pages/

