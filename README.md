Sigil
=====

Sigil is a free, open source, multi-platform ebook editor that uses
Qt (and QtWebEngine). It is designed to edit books in ePub format (both ePub 2 and ePub 3).


Links
=====

* Its website is located at http://sigil-ebook.com

* Its current code repository is located at https://github.com/Sigil-Ebook/Sigil

* Translations are located at https://www.transifex.com/projects/p/sigil/

* Support forums are located at http://www.mobileread.com/forums
    Select Sigil from the list of main forums

* Sigil Plugin Index (hosted by www.mobileread.com) at 
    http://www.mobileread.com/forums/showthread.php?t=247431

* Sigil User Guide is located at https://github.com/Sigil-Ebook/sigil-user-guide/releases/latest

Issue Tracker
=============

Please do not use the issue tracker to ask questions or suggest new features.  Both of the main developers
of Sigil monitor the Sigil Forum at https://www.mobileread.com/forums.
All questions and feature requests should be directed there so that other interested users can help or comment.

Issue tracking is intended for discussion around issues with the code. 
It is also intended for actual bug tracking.

Feature requests opened on the issue tracker will be closed.


Linux Build and Install
=======================

Starting with Sigil 2.0.2, the default cmake configuration is to build with Qt6. For a while, the latest versions of Sigil can still be built with Qt5 by passing the -DUSE_QT5=1 directive to cmake for the intial configuration.

For newer Linux systems like Ubuntu 23.04 (and its derivitives), or Arch Linux, or Debian Unstable, you should be able to compile Sigil using repo-provided dependencies. Instructions for doing so can be found in:

> [docs/Building_on_Linux_with_Qt6.md](./docs/Building_on_Linux_with_Qt6.md) ([or .html](./docs/Building_on_Linux_with_Qt6.html))

The Qt6 build documentation is Arch-centric (as that is the distro I've built Sigil on for quite a few years now). Apologies to other distros. The slight is not intentional. Time has simply moved on, and the dependency package naming conventions are no longer familiar to me. I'd be happy to host community-supplied build instructions for other distros.

For older Linux systems whose software repositories do not provide Qt6.2.3 (or higher), the
detailed instructions for building/installing Sigil with Qt5 can be found in:

> [docs/Building_on_Linux.md](./docs/Building_on_Linux.md) ([or .html](./docs/Building_on_Linux.html))

An up-to-date version of Sigil is available via flatpak on Flathub. So if your distro can use Flatpak, you can always use [Sigil that way](https://flathub.org/apps/details/com.sigil_ebook.Sigil) if your distro's Sigil package seems to be lagging too far behind.

For Building on Mac OS X
========================

Building using purely XCode is no longer supported on Mac OS X.  The easiest 
way to build Sigil on Mac OS X is to use cmake 3.X and the XCode CommandLineTools.   

Also because Sigil now embeds Python 3.11.3, see  

> [docs/Building_A_Relocatable_Python_3.11_Framework_on_MacOSX.txt](./docs/Building_A_Relocatable_Python_3.11_Framework_on_MacOSX.txt)

for detailed instructions on how to build a fully relocatable Python 3.11.3 framework before
building Sigil.  

For official releases Sigil uses Qt6.5.3  plus official cve and local patches see:  

> [docs/Building_Qt6.5_From_Source_on_MacOSX.txt](./docs/Building_Qt6.5_From_Source_on_MacOSX.txt)

Sigil master now supports building with Qt-5.10.X through to Qt-6.5.3.  For older Qt5 see:

> [docs/Building_Qt5_From_Source_on_MacOSX.txt](./docs/Building_Qt5_From_Source_on_MacOSX.txt)

And finally to build Sigil itself see:

> [docs/Building_Sigil_On_MacOSX_With_Qt6.txt](./docs/Building_Sigil_On_MacOSX_With_Qt6.txt)

and for building Sigil under the older Qt5 see:

> [docs/Building_Sigil_On_MacOSX_With_Qt5.txt](./docs/Building_Sigil_On_MacOSX_With_Qt5.txt)



For Installing/Building on Windows
==================================

Sigil currently provides a Windows installer for x64 and will work on Windows 10 (1809) or newer.

The latest Sigil versions are also typically available via the [winget (Windows 10+)](https://winstall.app/apps/Sigil-Ebook.Sigil), [Chocolatey (Windows 10+)](https://community.chocolatey.org/packages/Sigil), and [Npackd](https://npackd.appspot.com/p?q=sigil) Windows package managers. There are no "scary" Microsoft warnings about unknown publishers if you install Sigil via one of these package managers. 

To build Sigil on Windows yourself, see:

> [docs/Building_Sigil_on_Windows_with_Qt6.md](./docs/Building_Sigil_on_Windows_with_Qt6.md).



License
=======

Sigil is licensed under the GPLv3. The complete license is located in
COPYING.txt.

Note that libraries and components Sigil used and bundles may use a different
license (that is compatible with the GPLv3) from Sigil. See the specific
component for their respective license.  The source code from these
projects can be found under Sigil/3rdparty unless otherwise indicated.  
Please see their respective folders for complete license information.

Currently these projects include:

* Hunspell 1.7.2 - https://github.com/hunspell/hunspell
* MiniZip version 1.1 (plus some security changes)
* Perl-compatible Regular Expression Library 2 (pcre2 version 10.39)
* ZLib Data Compression Library (zlib 1.2.13)
* jQuery-3.6.4 (src/Resource_Files/javascript/jquery-3.6.4.min.js)
* jQuery.ScrollTo-2.1.2 (src/Resource_Files/javascript/jquery.scrollTo-2.1.2.min.js)
* MathJax.js Version 3.2.X [required minimum is 3.2.2]: (src/Resource_Files/polyfills)

In addtion, Sigil uses the following other packages that have been specifically
modified for use inside Sigil:

* Beautiful Soup 4 (src/Resource_Files/plugin_launchers/sigil_bs4)
* Sigil-gumbo based on Google's Gumbo Parser (internal/gumbo)



Sigil in Action
===============

![Sigil](docs/screencaps/sigil.png?raw=true) Sigil Main Window
    

![Sigil Dark Mode](docs/screencaps/sigil_dark.png?raw=true) Dark Mode


![Generate TOC](docs/screencaps/generate_toc.png?raw=true) Generate ToC


![Plugins](docs/screencaps/manage_plugins.png?raw=true) Python3 Plugins


![Edit Metadata](docs/screencaps/edit_metadata.png?raw=true) Edit Metadata


![Reports](docs/screencaps/reports.png?raw=true) Run Reports


![Checkpoint Compare](docs/screencaps/checkpoint_compare.png?raw=true) Detect Changes


![Preview Inspector](docs/screencaps/preview_inspector.png?raw=true) Preview's Inspector


![Custom Layout](docs/screencaps/sigil_custom.png?raw=true) Customize Your Layout


![Validation](docs/screencaps/validation_via_plugins.png?raw=true) Validate EPUB, CSS, XHTML, etc.


![PageEdit Companion Program](docs/screencaps/pageedit.png?raw=true) Interface to PageEdit Visual XHtml Editor




Package Versions of Sigil
=========================

[![Packaging status](https://repology.org/badge/vertical-allrepos/sigil.svg)](https://repology.org/project/sigil/versions)
