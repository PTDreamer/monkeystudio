# Release 1.9.0.0 #

Monkey Studio IDE is a cross platform Integrated Development Environment.
It run on Windows (98 up to Seven), Mac OS X (Universal ppc/x86 for 10.4 up to 10.6), Linux and Unix like.

# Changes since release 1.8.4.0 #

  * Complete rewrite of the XUP internals.
  * Complete rewrite of the projects settings editor (they now use abstract classes and shared code).
  * QScintilla updated to last version.
  * Small GUI revamp.
  * A file can now be opened as brut text file.
  * Add a new workspace mode (specially for Mac OS X, NoTabs has been replaced by MDI, NoTabs is the new mode).
  * Qt Version manager now better discover installed Qt version.
  * Build Steps has been updated and now handle better the warnings/messages/errors. In addition, the qmake output parser has been introduced plus the gcc/make parsers have been totally rewritten.
  * Plugins about dialog has been reworked.
  * Message boxes plugins has been reworked, the command box diseappear.
  * Added the possibility to open as plain text the current project file.
  * Custom project action are now available for all kind of projects, in addition, the qmake plugin now read the project makefile for better discovering the available build rules.
  * Added and reworked many templates.
  * The dock widgets vertical state of their title bar is now saved/restored.


# Screenshots #

![http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.9.0.0_plugins_about.png](http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.9.0.0_plugins_about.png)<br />
(The new about dialog of plugins)<br /><br />
![http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.9.0.0_qmake_translations.png](http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.9.0.0_qmake_translations.png)<br />
(The new project settings editor for qmake, especially, the translations handler page)<br /><br />
![http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.9.0.0_templates.png](http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.9.0.0_templates.png)<br />
(The templates wizard)<br /><br />
![http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.9.0.0_mainwindow.png](http://monkeystudio.googlecode.com/svn/wiki/images/cl_1.9.0.0_mainwindow.png)<br />
(The main window)