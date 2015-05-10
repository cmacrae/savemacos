About
-----
A streamlined bootstrapper for getting [pkgsrc](http://pkgsrc.net)/[pkgin](http://pkgin.net) up and running on OS X, fast!

Why?
----
Why wait for other ports/package managers to compile your software?
With [pkgin](http://pkgin.net), you get GPG signed binary packages - fast and secure!

Installation
------------
To get started, grab a copy of the repo (either clone it, or download as a zip), open up a terminal and simply run the `bootstrap` script - you'll be up and running in under a minute!

[Here's a quick demo of the script in action](https://youtu.be/oMWo3nouUsE)
[![Save OS X Demo](http://i.imgur.com/F06pnfl.png)](https://youtu.be/oMWo3nouUsE)

So what does this script do?
----------------------------
In a nutshell, this script will install [pkgsrc](http://pkgsrc.net), [pkgin](http://pkgin.net), add [Joyent](https://github.com/joyent)'s package repo, and set up your PATH & MANPATH evaluation.

Unobtrusive
-----------
[pkgsrc](http://pkgsrc.net) won't pollute your system by inserting libraries here and there, or dotting files all over the place.
Installation is confined to a very select few directories, namely: `/usr/pkg` & `/var/db/pkgin`

Want to uninstall [pkgsrc](http://pkgsrc.net)/[pkgin](http://pkgin.net)? It's as easy as:  
`sudo rm -r /usr/pkg /var/db/pkgin /etc/{man,}paths.d/pkgsrc`

pkgin usage
-----------
Want to find and install a package?

`pkgin search <package name>`

`sudo pkgin install <package name>`

Nice 'n easy!

See [here](http://pkgin.net/#examples) for pkgin's usage examples.

Why choose pkgsrc/pkgin over \<insert package manager here\>?
-----------------------------------------------------------------------------
Here's a list of just a few properties that make [pkgin](http://pkgin.net/) (a binary package manager for pkgsrc) different from other package managers available for OS X:
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

Thanks
------
Packages are now generously hosted by [Joyent](https://github.com/joyent) and built by [jperkin](https://github.com/jperkin).

Contact
=======
**IRC**: For all things pkgsrc, head over to `#pkgsrc` on freenode

License
-------
Use of this source code is governed by an ISC license that can be found in [the LICENSE file](LICENSE)
