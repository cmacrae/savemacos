Save OS X
=========
The official repo for the [Save OS X](http://saveosx.org/) project's bootstrapper.

About
-----
[Save OS X](http://saveosx.org/) is a hacking and development project for Apple’s Operating System: OS X.
We’re geared towards bringing a wealth of software that’s often found on other UNIX derived OS’s to OS X and showing the user that they can use OS X as a great UNIX based workstation.

Why?
----
To put it simply: because OS X is capable of much more than is immediately apparent to the average user. It has a familiar set of underlying utilities, many taken from the various BSD projects. We want to complement these with other tools available.

We want to show people that OS X is a perfectly viable option for developers, sysadmins, hackers, or just those who like to tinker.

Installation
------------
To get started, grab a copy of the repo (either clone it, or download as a zip), open up a terminal and simply run the `bootstrap` script - you'll be up and running in under a minute!

[Here's a quick demo of the script in action](https://youtu.be/oMWo3nouUsE)  

So what does this script do?
----------------------------
In a nutshell, this script will install [pkgsrc](http://pkgsrc.net), [pkgin](http://pkgin.net), add our package repo, and set up your PATH & MANPATH evaluation.

If you're familiar with shell, peruse through the code, it should be pretty clear what's happening :)

Unobtrusive
-----------
Save OS X won't pollute your system by inserting libraries here and there, or dotting files all over the place.
Installation is confined to a very select few directories, namely: `/usr/pkg` & `/var/db/pkg*`

Want to uninstall Save OS X? It's as easy as: `sudo rm -r /usr/pkg* /var/db/pkg*`

pkgin usage
-----------
Want to find and install a package?

`pkgin search <package name>`

`pkgin install <package name>`

Nice 'n easy!

See [here](http://pkgin.net/#examples) for pkgin's usage examples.

Why choose Save OS X (specifically pkgin) over \<insert package manager here\>?
-----------------------------------------------------------------------------
Here's a list of properties that make [pkgin](http://pkgin.net/) (a binary package manager for pkgsrc) different from other package managers available for OS X:
- Precompiled packages from a trusted source
- Signed pacakges with GPG
- Dead simple makefiles
- A robust multi platform framework
- Can be bootstrapped without any external dependencies other than a C compiler & a shell
- Tried and true, with a huge community of BSD developers behind it (and many devs from other communities)
- A very large collection of packages (up to 15,000)
- Ultra portable framework for use on many other OS's results in high quality ports
- Easy creation of new ports/packages
- Source code & package management are kept separated

Who?
----
[Save OS X](http://saveosx.org/) is a collaborative project between [Calum MacRae](https://github.com/cmacrae) and [Youri Mouton](https://github.com/yrmt)

**E-mail:** [calum0macrae@gmail.com](mailto:calum0macrae@gmail.com) / [youri.mout@gmail.com](mailto:youri.mout@gmail.com)

**IRC**: Come join us at `#saveosx` on `irc.oftc.net`

**Twitter**: [@calumacrae](https://twitter.com/calumacrae) / [@YouriMouton](https://twitter.com/YouriMouton)

License
-------
Use of this source code is governed by an ISC license that can be found in [the LICENSE file](LICENSE)
