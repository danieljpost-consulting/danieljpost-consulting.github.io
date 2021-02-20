---
layout: default
title: Lessons learned while playing with Jekyll
---
# Lessons learned while playing with Jekyll

Perhaps if I write em down I will not repeat them - TODO: add laughing gif here

## Lessons Learned: setting up locally
* Raspberry Pi linux, i.e. "Raspbian", is the best little Ubuntu I've played with. While I bet I would have done just as well on any other Ubuntu, this is working flawlessly and that makes me happy
* It helps to actually [read the instructions](https://jekyllrb.com/docs/installation/ubuntu/) when setting up rather than assuming it's going to be straightforward
* install the things locally so you don't end up using `sudo` all the time, which breaks things - this goes double for node / npm et al BTW
* .gitignore is going to be my friend here
* copypasting html into vim never goes well
* running jekyll serve runs the site on port 4000 which apparently isn't shared with the rest of my network?
* this is a good-enough excuse to start using name-based virtual host (I think I've got that wrong) via NGINX to give me what I want.
    * server\_name local.danieljpost.consulting;
    * root /var/www/ldc; # which is a symlink
* apparently we can't have nice things - I may have to run `jekyll doctor` repeatedly and install all the gems locally, manually, until it actually works
* it's all lies - I can't get the damn jekyll to actually parse my html files. Yet. Stealing Gemfile from rubyonrails.org to see if that helps
* I don't know why it's not munging tips/Jekyll.md to an html file -- yet.
* answer: because I didn't read the damn "front matter" page, which is after the Liquid page
* `jekyll build --watch` is the best. The `--incremental` flag might seem like a good idea until you want to change a header or footer or configuration variable and can't understand why it's not updating.
* I'm going to have to put actual thought into color schemes rather than just arbitrarily start fucking with reversing the default colors
* There's a wealth of good examples to be stolen from the uswds-site documents I've now bookmarked and forked onto GitHub
* I haven't yet put these into a codesandbos, but that's imminent. Perhaps Saturday
* I might just steal the USWDS website and present it as my own work at .solutions or .consulting
* Will need to revisit that, when I'm rested. Learning to Learn has taught me that I should do these things in little steps with little spaces between
* also, played with dyslexia font. Need to write that up.
* the doc subdirectory of danieljpost.pro was automagically jekyll'd without me intending it, and I want to figure out how to make the whole site work that easily
* spent a bit of time playing with Google Analytics and Google Tag Manager. I think it's actually working now at (danieljpost.pro)
* ci has been breaking the entire time on danieljpost.gihub.io (danieljpost.info) and I had forgotten to notice it
