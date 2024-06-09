---
title: Previewing a GH Pages site locally
author: Atirut Wattanamongkol
---
...a.k.a. "why is Ruby package management so damn convoluted?"

And I'm not answering that question, by the way, because I actually asked that.

Now that I've got my own blog site up, being able to preview changes locally without waiting for GitHub's Actions container to spin up quickly became essential. Did I finally do it? Well, yes! I had to jump through quite a few hoops, but it's possible.

If you're looking to start your own GH Pages blog, I hope this will help you get started with the local stuff. Let's start the journey, shall we?

## The basics

First off, install `gem`...
```bash
sudo dnf install rubygems ruby-devel
```
See that development package? That will be important for installing packages via `gem` later on, and `rubygems` doesn't have it as a dependency for some reason.

Now install `bundler` and `jekyll`
```bash
gem install bundler jekyll
```

## The Bodge:tm:

Now, by default, GitHub actually allow you to omit *a lot* of files that would be necessary for previewing files locally, the most important one being `Gemfile`. So, run `jekyll new <insert site name here>`, navigate into the generated directory, rip out `Gemfile` (and optionally, `.gitignore`) into your actual site, and disgard the rest of the generated directory into your local recycle bin.

Then, open up `Gemfile` in whatever text editor you use (I won't judge), and...
- Remove or comment out the line that says `gem "jekyll", "~> 4.3.3"`. It should be on line 10.
- Uncomment `gem "github-pages", group: :jekyll_plugins`. It should be on line 15.
- Update the installed packages by running `bundle install`.

After all that, install our final secret dependency by running `bundle add webrick`. Now, you should be able to run `bundle exec jekyll serve`, click on the link it spits out, start working on your site locally.
