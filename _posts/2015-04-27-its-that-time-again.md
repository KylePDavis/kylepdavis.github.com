---
tags: health yard mongodb electron docker joyent triton
---


### personal

- healthier me
    - have lost 11.7 lbs so far
    - tracking my food via MyFitnessPal
    - walking extra when I can (I like gamification, so this is "earning taste points")
    - just reduced my caloric intake by another 200 to go even faster
- yard work: part C
    - done: mow (grows so fast in Spring)
    - pending: mulch, flowers, cutting down extra trees and shrubs
    - success: spray for bugs is working on bag worms (didn't see that coming)
    - grrr: dandelions are everywhere, birds trying to build nest in my grill


### projects

- `mongodb-workbench` (aka `mw` (formerly `mongosaurus`))
    - trying out `electron` from the Atom project rather than `nw.js` (actually started working on this while it was still `atom-shell`)
    - refactored "server" and "database" to use plugins for sub-sections
    - pending: refactoring "collection" tab to use plugins for sub-sections
    - toying around with using `gulp`, `babel`, `less`, `uglify`, etc. for building an actual release files
- `docker`
    - a nice way of quickly spinning up Linux-based VMs
    - great for simplifing complex local development environments
    - amazing for deployments to test and production environments -- with this why would I ever want something like `chef`?  :-)
    - `kitematic` is a nice introductory UI that helps simplify some of the extra complications involved with docker container mangement on Mac OS X (due to having to use `boot2docker` between the `VirtualBox` VM and your actual docker containers)
    - curious if it could use VMs via the built-in Mac OS X Yosemite hypervisor (lighter weight? would just be a new `docker-machine` target probably)
    - suspiciously like SmartOS images but with tools that are a bit more developer oriented
    - excited to try the new docker stuff from Joyent, aka `Triton`, but still waiting on my early access to the beta program to kick in  :-/
