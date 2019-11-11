---
title: "You know it if you already knew it: reviving my github.io page"
author: trort
excerpt_separator: "<!--more-->"
categories:
  - Blog learning path
tags:
  - Jekyll
  - github-pages
last_modified_at: 2019-11-10
---
For some reason, I had the idea this afternoon to revive my github page after more than two years. It turns out to take much longer than I expected. I was even so frustrated at one point that only playing games helped me to continue. So it might be a good idea to document what happened.
<!--more-->
# Add a theme
Official document is [here](https://help.github.com/en/github/working-with-github-pages/adding-a-theme-to-your-github-pages-site-using-jekyll). 
Do not use the ones listed in settings. They are just too bad. 
Jekyll has a list of nice themes or sites [here](https://github.com/jekyll/jekyll/wiki/sites), where you can find good ones and fork them, except there are too many there (and some are no longer accessible!).
Anyway, I found the [so-simple-theme](https://github.com/mmistakes/so-simple-theme) which I really like from that long list.
> Hint: the way to use it is as simple as adding `remote_theme: "mmistakes/so-simple-theme@3.2.0"` to `_config.yml`. I just didn't figure that out.

So I cloned it to start testing...

# Set up so-simple-theme
The official guide starts [here](https://github.com/mmistakes/so-simple-theme#github-pages-method), and I got totally lost at step 1 (what is gem and where is that line?).
After cloning the repo, things got more disastrous as I was overwhelmed by all the files and folders.
There was a list of files to delete if you are running Jekyll yourself.
But for using on github, all you need to copy is the `_config.yml` file in either `docs` or `example`.
(Those are the examples for *using* this theme, while the repo itself is the source code *defining* theme.)
Some additional settings are through files in the `_data` folder.
And all other files are pretty much examples for you to play with.

# Test on a local host
To test the theme and all pages on localhost, [here](https://help.github.com/en/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll) is a guide from GitHub.
The prerequisites part is not super easy to understand if you have no idea what is what (and may not be needed if you already know Jekyll well).

So here is what I did:
1. Install Ruby. Download [here](https://rubyinstaller.org/downloads/). The without-devkit version seems perfectly fine here.
2. Install Bundler by running `gem install bundler`.
3. Add a file called `Gemfile` in the git dir with the following.
```
source 'https://rubygems.org'
gem "github-pages", group: :jekyll_plugins
```
For the sake of properly using Jekyll on localhost, add the gem "github-pages" is almost sufficient, but the theme may require additional plugins, giving the group part.
4. Run Jekyll locally with `bundle exec jekyll serve`. Changes to normal pages should be reflected immediately, except changes to `_config.yml`.
5. Make changes, commit, push, and done.


This is where I am right now. Hope more posts will show up soon.