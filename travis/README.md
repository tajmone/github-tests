# Travis Tests

This folder is used to test [Travis CI] using Windows OS and custom binaries for the build/test system.


-----

**Table of Contents**

<!-- MarkdownTOC autolink="true" bracket="round" autoanchor="false" lowercase="only_ascii" uri_encoding="true" levels="1,2,3" -->

- [File Contents](#file-contents)
- [Overview](#overview)
    - [The Problem](#the-problem)
    - [The Solution](#the-solution)

<!-- /MarkdownTOC -->

-----

# File Contents

- `/_dev/AlanSDK/` Alan SKD precompiled binaries
- `/alan-test/` — various test adventures (some fail)
- `build.exe` — custom builder and validator.


# Overview

This Travis test was designed to simulate the actual build system for a project I'm working on:

- https://github.com/alan-if/alan-by-examples

That is a repository containing text-adventures examples, and I need to ensure that all adventures submitted by pull requests meet certain criteria. In order to validate them I need to compile and run them using the ALAN compiler and interpreter.

## The Problem 

The problem with the build system is that ALAN binaries are only available as 32 bit applications, and that being in beta stage they are not available for Linux systems via package managers.

Another problem is that Travis only supports x64 architecture, and relies on Ubuntu for Linux distros. After the recent announcement that Canonical was going to [drop 32-bit support from Ubuntu] — which resultud in [Steam announcing that it will stop supporting Ubuntu], and Canonical backtracking on its decsion —  Ubuntu doesn't seem any longer a reliable OS to use with 32 bit apps.

Which means that using the new Windows OS (beta feautre) of Travis is a safer option, for Windows (unlike Ubuntu) will always support running 32-bit apps on a x64 machine.

## The Solution

I need to test how Windows OS can be used on Travis.

Specifically, I'll be using my custom `build.exe` binary tool to run all the build and checks operations in the repository, and I'll be keeping the `.exe` binaries in the repository itself (for practical reasons, because I also want end-users to build locally using a specific version of the AlanSDK).



<!-----------------------------------------------------------------------------
                               REFERENCE LINKS
------------------------------------------------------------------------------>

[Travis CI]: https://travis-ci.com "Visit Travis CI website"
[ALAN]: https://www.alanif.se/ "Visit ALAN website"

<!-- Ubuntu drops x32 support -->

[Steam announcing that it will stop supporting Ubuntu]: https://www.engadget.com/2019/06/22/steam-will-stop-supporting-ubuntu-linux/
[drop 32-bit support from Ubuntu]: https://www.engadget.com/2019/06/24/canonical-ubuntu-linux-32-bit-support/

<!-- EOF -->