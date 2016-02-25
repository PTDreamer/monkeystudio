# IDE Features #
IDE is a shortcut for Integrated Developing Environment, in other words, it provides more than script editor for writing the script.<br /> In our IDE, MonkeyStudio IDE, we provide different languages support<sup>(1)</sup>, script debugging<sup>(2)</sup>, syntax highlighting, building tools, project interfaces, built-in IRC client & so much more. discover our IDE ;)<br />

# IDE Main Parts #
the next image shows the main parts of the MkS<sup>(3)</sup> IDE:<br />
![http://monkeystudio.googlecode.com/svn/wiki/images/snapshot1.png](http://monkeystudio.googlecode.com/svn/wiki/images/snapshot1.png)

## Menubar ##
The menubar of the MkS IDE handles the standard IDE menus & submenus --it's another menubar. here's a quick description of each menu & its items:<br />

### File Menu ###
File menu contains the standard file actions, such as, opening, closing & saving actions. Here's a reference for this menu:<br />
  * New: creates a new file, the file type is then selected as of the file types dialog.
  * New Text File: creates a new plain text file.
  * Open: opens a file that its type is supported by MkS.
  * Recent: lists the last opened files.
    * clear: clears recent files list.
  * Session: contains the session management actions.
    * Save: saves the current session, including its opened projects files & GUI settings.
    * Restore: restores a pre-saved session.
  * Save: contains the file saving actions.
    * Save: saves the current file.
    * Save All: saves all opened files in the current session.
  * Close: contains the file closing actions.
    * Close: closes the current file, if not saved, then a save message is shown.
    * Close All: closes all the opened files, if a file is not saved, then a save message is shown.
  * Save as Backup: saves a backup copy of the current file.
  * Quick Print: prints the current file with the default used settings.
  * Print: shows the printing dialoge.
  * Quit: quits the MkS IDE.

### Edit Menu ###
Edit menu contains the code & IDE editing actions. the menu reference is:<br />
  * Settings: shows the IDE settings dialog.
  * Shortcuts Editor: shows the shortcuts editor dialog.
  * Translations: changes the current IDE language.
  * Undo: undoes the last action.
  * Redo: redoes the last undid action.
  * Copy: copies the selected part of the text.
  * Cut: cuts the selected part of the text.
  * Paste: pastes the text handled in the clipboard.
  * Search and Replace: contains the text search & replace actions.
    * Search in the file: search the current file for a matched text.
    * Replace in the file: replaces the matched text from the current file with the replace value.
    * Search in the folder: search the current folder files for a matched text.
    * Replace in the folder: replaces the matched text from the folder files with the current replace value.
  * Go To: goto a specified line.
  * All Commands: ...
  * Bookmarks: contains the bookmarks list.
  * Expand the Appriviation: expands the used appriviations in the code.
  * Prepare APIs: use the current project API to extend to create a new API.

### View Menu ###
View menu contains the actions for changing the current view of the IDE. the menu reference is:<br />
  * style: contains a list of GUI styles to choose between them.
  * Next Tab: move the activity to the next opened tab.
  * Previous Tab: move the activity to the previous tab.
  * Set Focus to Editor: whenever your cursor is focusing outside the editor, you can use this action, or its shortcut<sup>(4)</sup> (Ctrl + Return) to set the focus to the code editor.
  * Show Next Error: if you are debugging a code, this will move to the next error.

### Project Menu ###
Project menu contains all the actions needed to take control of a project, it contains:<br />
  * New Project: opens the new project dialog.
  * Open Project: opens the dialog to open a pre-created project.
  * Close Current Project: closes the current project & all of its resources.
  * Close all Projects: closes all opened projects & all of the opened resources.
  * Edit Current Project: opens the dialog of the project properties.
  * Add Existing Files to Current Project: opens the open dialog to choose files to add to the project.
  * Remove Files from Current Project: removes the selected files from the project resources list.
  * Recent: lists the last used projects.
    * clear: clears recent projects list.

### Tools Menu ###
Tools menu is the menu which handles the tools feature of MkS. It contains:<br />
  * Edit User Tools: opens the user tools dialog to edit the user tools.
  * Edit Desktop Tools: opens the desktop tools dialog to edit the desktop tools.
  * User Tools: lists the user tools.
  * lists the desktop tools.
to know more about the tools feature, please refer here.

### Plugins Menu ###
Plugins menu handles the plugins extra actions. This menu contains:<br />
  * Manage: the root menu of managing plugins.
    * Manage Using Dialog: opens the plugins managing dialog.

### Window Menu ###
Window menu contains extra actions to configure the GUI windows view. It contains:<br />
  * Single Document Interface: this action will set the windows view mode to the tabbing Interface.
  * Multiple Document Interface: this action will set the windows view mode to the classical windows Interface.
  * Top Level Windows Interface: this action will separate the windows from the IDE.
  * Cascade: cascades all windows.
  * Tile: tiles all windows.
  * Minimize: minimizes all windows.
  * Restore: restores all minimized windows.

### Docks Menu ###
Docks menu contains a set of dockable panels to show or hide them. to know more about docking in MkS continue to [#Dockbar](#Dockbar.md).<br />

### Help Menu ###
The classical help menu, which contains:<br />
  * About: opens the about dialog which contains semi-detailed information about the MkS.
  * About Qt: opens a dialog containing basic information about Qt GUI toolkit.

## Toolbar ##
This customizable bar provides you a good way to have more time by setting the frequently used actions in that bar.

## Dockbar ##
In MkS IDE, there's a placeholder for 4 dockbar placeholders. These placeholders can handle a set of float panels to show the MkS IDE GUI as you wish. In default, 3 dockbar placeholders are only enabled which are:
  * Top Dockbar: in default it doesn't handle any widget or panel, but you can let it handle some of them.
  * Left Dockbar: which handles:
    * Projects: this panel shows the projects list that are created or opened with MkS IDE.
    * File Browser: a simple file browser.
    * Widget Box: handles the Qt Widgets for using them when designing the GUIs.
  * Bottom Dockbar: which handles:
    * Build Steps: if you use MkS to build your projects, this panel will return the build log.
    * Output: if you run your project directly from MkS IDE you'll find here the executing output.
    * Commands: this panel logs the log of each command entered in the output panel.
    * Search and Replace: Quick Search and Replace actions.
    * Action Editor: this panel shows the actions used in the Qt GUI.
    * Signal/Slot Editor: this panel shows the signals & slots used in the Qt GUI.
    * Resources Editor: ...
  * Rigth Dockbar: which handles:
    * Class Browser: this lists the classes & methods of the current project.
    * Qt Assistant: a Qt help panel.
    * Object Inspector: lists the objects of the current project.
    * Property Editor: handles Qt GUI objects properties editor.


---

(1): we support C, Objective C, C++, Python & PHP till the moment.<br />
(2): for C, Objective C & C++ only till the moment.<br />
(3): MonkeyStudio.<br />
(4): it's a an alternative way to access the action from keyboard