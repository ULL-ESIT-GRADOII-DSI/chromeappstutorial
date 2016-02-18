Preface
======

This book explains in detail what a Chrome App is, but briefly, its relationship to Chrome is the same as a Windows app to Windows, or a Mac app to OS X: an app that you install on the platform and that makes use of application program interfaces (APIs) unique to that platform. This would be obvious but for the fact that the platform in this case, Chrome, is better known as a web browser and most of the “apps” that you run on it are really just fancy web pages. I’m thinking of Gmail, Facebook, Amazon, and a zillion others. Hence the confusion.

Why consider programming a Chrome App at all? Here are two good reasons:

* They’re portable across all of the major operating systems: Windows, Mac OS X, Linux, Chrome OS (for Chromebooks and Chromeboxes), and, with some restric‐ tions, even Android and iOS.

* Although web apps are equally as portable, they can’t access the local computer as Chrome Apps can. The most important example of this is that Chrome Apps can access the computer’s filesystem, just as native apps can.

I’m unable to think of any other platform that offers these two advantages.

With the good comes the not-so-good. Here are the chief disadvantages of Chrome Apps:

* On desktop operating systems, they run only under Chrome (although they can have their own launch icon and they appear to run standalone).

* Although the Chrome API is extensive and growing, it isn’t even close to encapsulating every native API.

