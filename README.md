# Compiler Compiler SpiderMonkey Playground

![img](https://pbs.twimg.com/media/EcZ_esIWsAAIrs8?format=jpg&name=large)

Welcome! You are likely here as part of the [Compiler Compiler Stream](https://www.twitch.tv/codehag). This repository is a space for you to try out what 
you learned, by replicating bugs that are covered in the stream. If you want to watch old episodes no longer on twitch, you can view the [stream archive](https://www.youtube.com/playlist?list=PLo3w8EB99pqJVPhmYbYdInBvAGarDavh-)

What this repository is -> A complete copy of the Firefox codebase, including Spidermonkey. For our purposes, we are mostly interested in the `js` directory. Why the whole browser? It is a long story but basically it is difficult to completely separate Spidermonkey from Gecko and other Firefox components. 

Important technical stuff -> [Follow these instructions](https://firefox-source-docs.mozilla.org/js/build.html) in order to build SpiderMonkey. If you have problems,
create an issue. 

# Branchs and Branch Structure

* [Bug #1286997](https://github.com/codehag/compiler-compiler-dev/tree/bug-1286997)

This repository is organized around branches. Each branch enables a test that will fail when you try to run it. Information about the bug will be found in the 
README.md of that branch, so you will always know what you need to do, along with what kind of challenges you can expect on the way.

Once you finish a bug, you can open a pull request and have it marked. It won't be merged, it will just be marked as correct. If you have any issues or questions, please open an issue and I will try to answer. Also
as you gain experience, a great way to solidify your learning is to help others! So don't be shy about helping eachother as well.
