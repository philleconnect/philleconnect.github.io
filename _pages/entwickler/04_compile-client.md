---
layout: page
title: HowToCompile
permalink: /entwickler/HowToCompile
tags: Entwickler
lang: en, de
---

# **HOW**TO**COMPILE**

## PREREQUISITEs

To compile the PhilleConnect you'll need:

* [The Lazarus FreePascal IDE](http://www.lazarus-ide.org){:target="_blank"}
* A trunk snapshot of the [Lazarus Synapse Library](https://sourceforge.net/p/synalist/code/HEAD/tree/trunk/){:target="_blank"} (use the 'download snapshot' button)
* A clone of the Application's Github repository you want to compile, of course

## SETUP YOUR BUILD ENVIRONMENT

* Navigate to your clone and open the `.lpi` file with lazarus.
* Go to Packages -> load package file.
* Load the package file of synapse.
* Go to Project -> Project inspector.
* Check if all files are found, especially `ssl_openssl.pas` and `ssl_openssl_lib.pas` from synapse. If they are not found, remove and re-add them.
* Compile your program!

## WHAT ELSE DO I NEED?

You will need the OpenSSL library to run the programs.

* On Windows, we recommend to use the two `.DLL` files equipped with the [ClientSetup for Windows](https://github.com/philleconnect/ClientSetup-Windows){:target="_blank"}. However, you also can build your own, if you want.
* On Linux, please install the package `openssl-dev`
