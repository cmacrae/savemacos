Save OS X
=========
The official repo for the [Save OS X](http://saveosx.org/) project's set-up scripts.

![alt text](img/hexley.png)

About
-----
[Save OS X](http://saveosx.org/) is a hacking and development project for Apple’s Operating System; OS X.
We’re geared towards bringing a wealth of software that’s often found on other UNIX derived OS’s to OS X and showing the user that they can use OS X as a great UNIX based workstation.

Why?
----
To put it simply: because OS X is capable of much more than is immediately apparent to the average user. It has a familiar set of underlying utilities, many taken from the various BSD projects. We want to complement these with other tools available.

We want to show people that OS X is a perfectly viable option for developers, sysadmins, hackers, or just those who like to tinker.

Installation
------------
**Note:** *See [Here be Dragons](#here-be-dragons) before proceeding!*

To get started, grab a copy of the repo (either clone it, or download as a zip).
Open up a Terminal (this must be Apple's 'Terminal.app'), then `cd` to the `scripts` sub-directory and run the `bootstrap` script.

That should get you started.
Simple as that!

So what do these scripts do?
----------------------------
If you follow the steps in the [installation section](#installation), you'll be greeted by an interactive script.
In a nutshell, this script will walk you through the set-up of [pkgsrc](http://pkgsrc.net), [pkgin](http://pkgin.net), set up your PATH & optionally implement [X11](http://www.x.org/wiki/) (using [XQuartz](https://xquartz.macosforge.org/landing/)) in a seamless manner. 

If you're familiar with shell, peruse through the code, it should be pretty clear what's happening :)

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

Here be Dragons
---------------
This is still a work in progress, so please, for your own sake; **wait until I'm finished to run any scripts here** ;)

That said, testers are more than welcome! I've tested these scripts thoroughly on my systems, and nothing horrible has happened yet. So if you're up for it, dive in!
Feel free to raise an issue for any problems you may encounter, or submit a pull request if you feel something could be implemented better.

Who?
----
[Save OS X](http://saveosx.org/) is a collaborative project between [Calum MacRae](https://github.com/cmacrae) and [Youri Mouton](https://github.com/yrmt)

**E-mail:** [calum0macrae@gmail.com](mailto:calum0macrae@gmail.com) / [youri.mout@gmail.com](mailto:youri.mout@gmail.com)

**IRC**: Come join us at `#saveosx` on `irc.oftc.net`

License
-------
Use of this source code is governed by an ISC license that can be found in [the LICENSE file](LICENSE)
