hubdrop.github.io
=================
This repo is for a Jekyll blog, http://blog.hubdrop.io.


Development
-----------

To run this site locally, you need Jekyll.

Installing Jekyll isn't hard.  This was summarized from https://help.github.com/articles/using-jekyll-with-pages#installing-jekyll

1. Get Ruby, 1.9.3 or 2.0.0.

  Use `ruby --version` to check.
  Go to https://www.ruby-lang.org/en/downloads/ if you don't have it.

2. Install Bundler


    $ sudo gem install bundler

3. Install `github-pages` gem.


    $ sudo gem install github-pages

4. Get this repo.


    $ git clone git@github.com:hubdrop/hubdrop.github.io.git
    $ cd hubdrop.github.io

5. Run Jekyll server.


    $ bundle exec jekyll serve --watch

  The `--watch` option will make changes visible in the browser immediately.
