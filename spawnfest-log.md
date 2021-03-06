Spawnfest Acitivity Log
=======================

ferd, July 6, 22:00 EST: initial commit, starting this log. Orbitz is off to sleep because he's now a Swede. I'm starting this repo to get some more useful time out of my day. Trying to get a basic directory structure in place.

ferd, July 6, 22:20 EST: I've decided to try and get some test structure and scaffolding up and running. We might never use it, but it'll likely be useful to test shit and get faster later. I'm choosing CT. No idea if Orbitz knows about it, but he's sleeping so he loses by default. Worst case is I have to maintain all tests alone.

ferd, July 7, 00:47 EST: The test suite now contains a basic Cowboy-based server that can serve beam files, erl files, zipped OTP apps (compiled), and .ez archives (well, just one of each type). There is no actual test in there, but it's a nice stepping stone to get moving. We'll still have to add some HTML-serving function so we can parse for links in the page, eventually redirecting to the flat directories we need. Somewhat underwhelmed but still satisfied with the progress. 

ferd, July 7, 01:17 EST: Added basic HTML serving functions for all types in a link tag within the head of the page. Might want to change it to some 'a' tag with a specific 'rel' attribute, but so far that's what I decided to write. I'm calling it a night at this point. Hopefully the test scaffolding will provide a convenient base on which to speed up our development. The format I've picked for URLs does differ a bit from what was planned in the google doc planning we had made and imagined, but whatever. I'm tired and went with what I figured would be convenient as someone who would give access to files when writing a tutorial/demo.

ferd, July 7, 09:43 EST: After talking with Orbitz, it was decided to also support rebarized apps (or rather, apps with a Makefile provided). I've added tests for that. The .zip file is zippers-0.1.zip, my own zip library modified for the purpose. Judges: please see it as an app more than pre-written code, it's just to test working with rebar.  The file has no deps/ so we might need another one later on to test.

ferd, July 7, 13:17 EST: Managed to get Tend to boot up as an app file and get all paths set up right for existing libraries. I had to steal code server.erl code just to be able to do that thing right. It seems to work though, which is great.

ferd, July 7, 18:12 EST: busy day! Orbitz managed to write the code loading stuff, and we're now both working on getting files compiled. Things are going well.

ferd, July 7, 19:00 EST: Thank God for tests! Found out that SSL wasn't getting started correctly, and now that's it fixed, we can load gists on the fly from github through SSL and whatnot.

ferd, July 7, 20:25 EST: Incredible! We've done it! HTML pages, OTP apps and modules. All supported and loaded! And the canary in the shaft isn't dead yet!

ferd, July 7, 23:37 EST: Almost another day over. I've completed a code reloader, and after trying for very long to make it reload files, I remembered that I needed to make non-superficial changes for the version to be upgrade (adding comments and shit isn't enough). I've lost something like 30-40 minutes on that and I feel dumb. I blame being tired, but ultimately, it's probably all the fault of the OTP team for not preemptively reading my mind.

ferd, July 8, 01:42 EST: Ugh, it's late. I've found and fixed a couple of mistakes related to rebar handling, and added tests for all types of builds. It sucks that OTP apps that expect rebar to be globally installed won't be compileable, but too bad for them I guess. The tests are now taking forever to run, thanks to downloading and building 3 apps with their deps.

ferd, July 8, 09:29 EST: The Swedish fairy got me a surprise this morning; Orbitz has implemented a rebuild feature to complement the 'reload()' one. Here is some little modifications peppered over it. Oh and the Swedish fairy is *not* orbitz. Just re-read myself and realized how weird that sounded.

ferd, July 8, 09:55 EST: Holy moly, stuff works even with NIFs! We're both pretty satisfied at this point and we're working on polish. Malcolm (orbitz) is taking care of comments and specs, and I'm looking for writing docs and some demo code.

ferd, July 8, 11:01 EST: Clean up and polishing going well!

ferd, July 8, 15:23 EST: I guess we're pretty much done. We're now working on demonstrations of what _TEND_ can do, and otherwise, orbitz might be chasing a bug regarding circular references in a page; something without dire consequences, if not minor annoyances.

I will be logging off. Thanks for reading the development log. Now I'm gonna go try to rest and pretend I had a full week-end without programming, before going back to work and doing some more on Monday.

