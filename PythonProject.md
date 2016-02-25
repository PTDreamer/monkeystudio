# Introduction #

Python is a very popular interpreting programming language, it's developed to be an easy language with the features of the high level programming languages.<br />
As the python is getting more popular, a lot of the libraries that are designed originally for C & C++ had been ported to Python through binding libraries. One of these libraries is the PyQt which is the Python bindings for Qt. &, as MkS<sup>(1)</sup> supports Python language, it supports PyQt.

# PyQt notes #
PyQt is a multi-licensed Python library developed by RiverBank Computing Limited. For any use except for the commercial use, it's licensed under GPLv2. For the commercial use RiverBank computing provides a special-purpose designed commercial license.
For more information: http://www.riverbankcomputing.co.uk

# PyQt Hello World #
This part is a quick tutorial telling you how the basic things in PyQt are going.

## Notes ##
This tutorial expects that you have the basic knowledge in Python at least. If you don't know how the Python code looks like don't continue.

## Setup MonkeyStudio ##
The support of Python in MonkeyStudio is done through the [Python Plugin](pythonPlugin.md), thus, you need to verfify that the plugin is enabled at first.<br />
Goto: Plugins > Interpreter > Python, & check Enabled.

## Create The First Project ##
Now, you can create & open Python projects. Goto: Project > New, a Template Wizard will be shown. From the language menu choose Python. The left list will show you the Python projects templates MonkeyStudio provide, click on PyQt GUI. The right column of the dialog will show the set of settings needed to create the project. Change the project name to be: MonkeyStudio PyQt tutorial. Change the other options to fit your needs & click create.<br />
![http://monkeystudio.googlecode.com/svn/wiki/images/snapshot2.png](http://monkeystudio.googlecode.com/svn/wiki/images/snapshot2.png)

## Discovering the Project ##
Once you click create, the MkS will show you your created project. The projects Dockbar will show the project & its elements classified into two types: Qt Forms & Python Files. Qt Forms are the GUI forms you want to code, while, the Python Files are the codes. Expand Qt Forms & double click on mainwindow.ui, the Qt Forms designer will be shown. Activate the Widget Box dockbar to show the Qt GUI objects list & activate the Property Editor to show the objects properties bar. Change the windowTitle properety to: Hello World! to change the window's title.<br />
Now, put some objects to get some fun. Do something like this:<br />
![http://monkeystudio.googlecode.com/svn/wiki/images/snapshot3.png](http://monkeystudio.googlecode.com/svn/wiki/images/snapshot3.png)<br />
If you want to see how your form is displayed to the user, simply, click on 'Preview in..' button on the designer toolbar, & choose Preview in Oxygen or any other style.<br />
![http://monkeystudio.googlecode.com/svn/wiki/images/snapshot6.png](http://monkeystudio.googlecode.com/svn/wiki/images/snapshot6.png) the last button on the toolbar<br />
Now, we had the GUI ready for the coding. Return to the Project dockbar & double click on main.py. This will show the contents of the file. Lines description are as following:<br />
```
import sys

# import PyQt4 QtCore and QtGui modules
from PyQt4.QtCore import *
from PyQt4.QtGui import *
```
This part of the code imports the needed libraries to be able to start the GUI.

```
from mainwindow import MainWindow
```
This part imports the GUI windows & forms. In this case we are importing the Windows Named MainWindow written in file mainwindow[.ui].

```
if __name__ == '__main__':
```
This conditional syntax verifies that the program is a standalone & had not been ran as a subprocess.

```
    # create application
    app = QApplication(sys.argv)
    app.setApplicationName('!MonkeyStudio !PyQt tutorial')
```
This part prepares the Qt to show the windows.

```
    # create widget
    w = MainWindow()
    w.setWindowTitle('!MonkeyStudio !PyQt tutorial')
    w.show()
```
This part prepares the window we imported before, & shows it.

```
    # connection
    QObject.connect(app, SIGNAL('lastWindowClosed()'), app, SLOT('quit()'))
```
This part connects between the lastWindowClosed() signal & the quit() slot.

```
    # execute application
    sys.exit(app.exec_())
```
This part ends the program after executing the Qt application.<br />
Mostly, the main.py file is a standard file, we don't have a lot of things to do with it, because, the most hard work is in the mainwindow.py, which is the coding part of the form we created before. Now, open the mainwindow.py. Lines description are as following:<br />

```
from PyQt4 import uic

(Ui_MainWindow, QMainWindow) = uic.loadUiType('mainwindow.ui')
```
This imports the uic module from the PyQt library. This module is responsible from converting the UI file to something the PyQt can interact with.

```
class MainWindow (QMainWindow):
    """MainWindow inherits QMainWindow"""
```
This is the class block. Each form (or window) code part is a class which has functions.

```
    def __init__ (self, parent = None):
        QMainWindow.__init__(self, parent)
        self.ui = Ui_MainWindow()
        self.ui.setupUi(self)
```
This is the Class init function. It prepares the window.

```
    def __del__ (self):
        self.ui = None
```
This is the Class del function. It removes the window after closing it.<br />
This class is what exactly we will work on, because, in this class we will write how the window's Signals are being interpreted.

## CODING!!! ##
Before you start check [Signals & Slots](http://doc.trolltech.com/4.6/signalsandslots.html) page to know more about signals & slots.<br />
Let's start with an easy thing. When we click on Continue button we want the console to print something. To do so, we need at first to import a module from the PyQt4. Add this line to the head of the file:
```
from PyQt4.QtCore import *
```
Now, we need to connect the click() signal with a slot, by, adding to the end of the init function this line:
```
        self.connect(self.ui.pushButton, SIGNAL('clicked()'), SLOT('click()'))
```
This function connects the clicked() signal of the pushButton (the name of the button) with the click() slot. The click() slot in is not yet there, so, put this piece of code at the last of the class:
```
    @pyqtSlot("")
    def click(self):
        print "welcome, " + self.ui.lineEdit.text() + "!!"
```
The first line is a decoration telling the PyQt, that, this is a slot. The second line is the function defining line. The third line is the function body, in it, we put the print command to print greetings for the name written inside the lineEdit object.<br />
Now, all you need to do is playing with the signals & slots to get started.


---

(1): MonkeyStudio