# Release 1.8.4.0 #

Monkey Studio IDE is a cross platform Integrated Development Environment.
It run on Windows (98 up to Seven), Mac OS X (Universal ppc/x86 for 10.4 up to 10.6), Linux and Unix like.

# Changes since release 1.8.3.x #

  * New locale choice dialog.
  * New threaded Search & Replace plugin :
    * Incredibly quick and powerfull.
    * Search & replace in current file, opened files, project files, folders.
    * Has a settings widget.
    * The RegExp search now use Qt QRegExp instead of scintilla RegExp.
    * Replace can now do partial replace based on regexp capture id (see [here](SearchAndReplace.md)).
  * QScintilla updated to last version.
  * Add a new setting for set the default code editor font:
    * The font is mono-spaced by default.
    * All lexers are using the default font family and point size.
    * It's possible to update all lexers style elements to sync with default family & point size.
  * Qt Version manager now automatically discover installed Qt versions.
  * Class browser / qCtagsSense framework now based on ctags 5.8.
  * Tools has been moved to a plugin to strip the MkS core code.
  * Build Steps view is now using a custom model and does no longer freeze on heavy steps added in short lap of time.
  * Introduce a system environment variable in settings that allow to define/edit soem variables: NO CHANGES ARE MADE ON THE SYSTEM.
  * Translation files are now named using language/country code.
  * About dialog has been reworked.
  * Introduce a queued message widget:
    * Show passive informations to the user.
    * Possibility to add buttons and custom icons.
  * Rework the "Opened Files Dock" widget:
    * Support different sort methods.
    * Possibility to reload documents.
  * Introduce Update Checker plugin:
    * A plugin that inform and propose you to download new MkS releases.
  * XUP enhancements:
    * Dynamic Folder: a watched folder which contents is displayed inside the project view, with possible filter configuration.
    * Custom menu actions per project (Build, debug, interpret etc).
  * Fix a crash on non kde/qt based desktops.
  * Fix a long time unknown bug that cause build errors on (mostly) 64bits architectures.
  * Add support for Qt 4.7.
  * New Qt assistant plugin based on webkit that can now be used as a small web client.
  * PostIt plugin has been removed.
  * New templates for creating MkS plugins.
  * Introduce a file watcher plugin which track local/external file changes in the opened files view.


# Screenshots #

![http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.8.4.0_1.png](http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.8.4.0_1.png)<br />
(The new locale choice dialog)<br /><br />
![http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.8.4.0_2.png](http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.8.4.0_2.png)<br />
(The latest QScintilla version)<br /><br />
![http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.8.4.0_3.png](http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.8.4.0_3.png)<br />
(Qt version detection)<br /><br />
![http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.8.4.0_4.png](http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.8.4.0_4.png)<br />
(The RegExp Search & Replace)