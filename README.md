# Compiler Compiler BUG [#1286997](https://bugzilla.mozilla.org/show_bug.cgi?id=1286997)

This bug playground covers stream [episodes 1-6](https://www.youtube.com/playlist?list=PLo3w8EB99pqJVPhmYbYdInBvAGarDavh-).

The bug is captured by this test262 test: https://test262.report/browse/language/expressions/prefix-increment/S11.4.4_A6_T2.js

The core problem is that in Spidermonkey, the expressions `obj[key]++` evaluates differently  than
`obj[key]`. We can see this happen if we throw an error instead of key.

First, build spidermonkey by [following these instructions](https://firefox-source-docs.mozilla.org/js/build.html).

To run one of the tests for this, try this command in your console. `./mach jstests --shell js/src/build_DBG.OBJ/dist/bin/js
postfix`.

To see the solution for this, you can look through these [patches](https://phabricator.services.mozilla.com/D78905)

-----

Original text:

![img](https://pbs.twimg.com/media/EcZ_esIWsAAIrs8?format=jpg&name=large)

Welcome! You are likely here as part of the [Compiler Compiler Stream](https://www.twitch.tv/codehag). This repository is a space for you to try out what
you learned, by replicating bugs that are covered in the stream.

What this repository is -> A complete copy of the Firefox codebase, including Spidermonkey. For our purposes, we are mostly interested in the `js` directory. Why the whole browser? It is a long story but basically it is difficult to completely separate Spidermonkey from Gecko and other Firefox components.

Important technical stuff -> [Follow these instructions](https://firefox-source-docs.mozilla.org/js/build.html) in order to build SpiderMonkey. If you have problems,
create an issue.

This repository is organized around branches. Each branch enables a test that will fail when you try to run it. Information about the bug will be found in the
README.md of that branch, so you will always know what you need to do, along with what kind of challenges you can expect on the way.

Once you finish a bug, you can open a pull request and have it marked. It won't be merged, it will just be marked as correct. If you have any issues or questions, please open an issue and I will try to answer. Also
as you gain experience, a great way to solidify your learning is to help others! So don't be shy about helping eachother as well.
