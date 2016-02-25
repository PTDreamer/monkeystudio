# Introduction #

The class browser plugin allow you to browse your code quickly by presenting a tree of your source code.<br />It use our qCtagsSense framework which is based on a custom fork of Ctags project.

# Details #

Once you open a file that ctags can handle, a tree corresponding to your current file code will be populated.<br />
Clicking items of that tree will quick jump in your code. Context menus actions are available so you can go through implementations/declarations.<br />
As well opening a project will index all the project files.

A good feature we implemented is the possibility to search for tags (member, function etc) and see matching result into a separated tree.<br />
From there you can quickly jump to what you look for !<br />
The plugin has some settings that can be customized by the user:<br />

  * Integration Mode: Define how class browser is integrated into the IDE
    * Dock: A dock widget is added to the main interface and allow searching & quick jump.
    * Combo: A combobox is added to the context toolbar and allow to quick jump.
    * Both: Dock and Combo mode are available at same time.
  * Use physical database: Define if the database will be stocked on a physical file or in memory.
  * System include paths: This is a list of system paths to scan when the IDE starts, this paths should be paths that rarely changes.
  * Filtered file suffixes: A list of file suffixes used to forbids some files to be indexed.

The qCtagsSense framework is released as the same license as [MkS](http://monkeystudio.org).<br />
Our custom ctags fork can be checked out from our [svn](http://monkeystudio.org/Svn) and is released as same license as qCtagsSense.<br />
Ctags is a GPL project hosted at http://ctags.sourceforge.net