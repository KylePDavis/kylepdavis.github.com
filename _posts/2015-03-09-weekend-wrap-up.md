---
tags: database mongodb programming nodejs javascript es6 es7 babeljs typescript blog
---


### tech

In case you missed it, here are a bunch of things that I've been finding interesting lately:

- Joyent
    - [Building a better cloud with SmartOS + SmartDataCenter + Docker containers (aka VMs are stupid)](https://www.joyent.com/blog/container-service-preview)
    - [MongoDB 100-150% faster on Joyent vs AWS](https://www.joyent.com/public-cloud/benchmarks/mongodb)
    - [Elasticseach 50-70% faster on Joyent vs AWS](https://www.joyent.com/public-cloud/benchmarks/elasticsearch)
    - [PostgreSQL 15x faster on Joyent vs AWS](https://www.joyent.com/public-cloud/benchmarks/postgresql)
- JavaScript
    - [Angular2 drops AtScript and embraces TypeScript -- YAY!](http://dailyjs.com/2015/03/06/typekit-angular/)
    - [get all ES6 with Babel -- right now and it’s easy](http://babeljs.io/docs/learn-es6/)
    - [get just the async / await keywords -- right now and it’s easy](https://github.com/MatAtBread/nodent)
- MongoDB
    - I was able to use our 2.6 branches and use MongoDB 3.0 and reduce my data from 10 GB to 900 MB (initial scans went from 35s to 2.5s)


### projects

- [blogged](http://KylePDavis.com)
    - this blog
    - just got created
    - trying a different format:
        - all markdown
        - less text, more lists
    - hopefully easier to write and grok
    - writing content now and will try to write often
    - site does not actually work yet ... will fix soon :-/
- my pc lives... IT'S ALIVE!
    - finally got my new power supply and managed to revive my old PC after over a year of downtime - [Rosewill Lightning 800w](http://www.newegg.com/Product/Product.aspx?Item=N82E16817182063&cm_re=rosewill_lightning_power-_-17-182-063-_-Product)
    - got Linux up and running, updated from Ubuntu 14.04 to Ubuntu 14.10 w/o issue, want 15.04 but I can wait a few more weeks
    - eventually I'll go and fix Windows but that's going to be a nightmare because I was in the middle of moving data between drives to make use of my new SSD when things died and now I need to figure out exactly where I left off... ouch
- [git.KylePDavis.com](http://git.KylePDavis.com) -- finally got an updated [Gogs](http://gogs.io) after months of neglect
    - note to self: go add inline editing... I love that feature on GitHub and want it everywhere
- `argvee` - argv w/ extra enhancements for NodeJS
    - they're are way too many of these, so I'm building some more ;-)
    - as far as existiing ones go I like commander and nopt the best but I still think we can do better so I'm trying a few things out:
        1. try to do everything entirely object based to keep it simple and focus on the features
        2. try and do everything entirely string based to focus on the API and ease of usage
    - profit! -- well okay, maybe not, but I'll either try to release these separately or combine them into one awesome arg parsing library
- `gimme` - meta-installer to replace my old `.profile` script's `_install()` function
    - imported fixes from `_install()` in my [dotfiles](https://github.com/KylePDavis/dotfiles)
    - working pretty well in Linux
    - needs more testing in Mac OS X
    - need to split into separate package
    - got tab completion working
    - will get one-liner to `gimme gimme` soon
- `json-beautify` - json beautifier
    - nearly ready to release this thing
    - adding more tests
- `mongosaurus` - mongodb workbench tool
    - angularjs based but might switch to angularjs 2
    - node-webkit currently but toying around with atom-shell as a nicer alternative
    - done with basic connectivity and most of the collection APIs (insert, remove, find, aggregate)
    - more to come soon ...
