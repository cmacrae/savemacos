Main points of focus
====================

Whilst embarking on this marvelous journey, we've come to find that we're focussing on some key points that we feel need improving.

GUI
---

Apple are known for their attention to detail when it comes to design, and the same can be said for OS X's Graphical User Interface. Although many people like what they've done with it, we feel it gets in the way of getting work done, and at the same time manages to hog quite a bit of the systems resources.
Most users who are familiar with other Unix based operating systems, like *BSD & GNU/Linux will be familiar with the X11 graphical server. Naturally, this seemed like the perfect environment to implement in place of Apple's standard desktop.

Using the XQuartz application from Apple Open Source, and a few tweaks here and there, Save OS X seemlessly implements the X environment as any other system would. No dock, no menubar, no dashboard, no virtual desktops... just pure X (though, we do want to keep everyone happy, so Aqua applications can still be run parralel to your X11 applications, so don't panic!).

Using X means you can tailor your environment to your needs, it's just X, what more can we say?


Performance
-----------

OS X handles pretty good on most machines, though when you put it in the hands of two Unix hobbyists, who have some spare time on their hands and they start to dig, it quickly becomes apparent that there's really rather a lot of "stuff" running under the hood that just isn't necessary for the average user, and is almost offensive to those who might consider themselves above average.
Throughout our endeavours, one of our primary focuses is to trim away anything and everything that we deem useless/resource hungry - and of course, that's not to say one can't simply add back something they might miss.

