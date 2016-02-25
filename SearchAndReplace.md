# Introduction #

The MkS Search & Replace plugin adds the support of searching & replacing within files or directories.


# Details #
Search & Replace is a common features in most text editors & IDEs<sup>(1)</sup>. It allows you to search for a specified string in the current file, or in files in a specified directory & replace them with a specified string. That will help you override any mistakes or late-changes done to the whole project.

## Commands provided by the plugin ##
When the Search & Replace plugin is enabled, a set of commands will be added to View > Search & Replace, these are:
  * Search: to search in the current file.
  * Replace: to search & replace in the current file.
  * Search Next: to search for the next occurrences.
  * Search Previous: to search for the previous occurrences.
  * Search in Directory: to search in all files in a directory.
  * Replace in Directory: to search & replace in all files in a directory.
  * Search in Project Files: to search in all files in the current opened project.
  * Replace in Project Files: to search & replace in all files in the current opened project.
  * Search in Opened Files: to search in all files in all opened files.
  * Replace in Opened Files: to search & replace in all files in all opened files.

## Working with RegExp<sup>(2)</sup> ##
Search & Replace plugin provides searching & replacing with RegExp. RegExp is a logical string that is used for matching a string according to a logical pattern not a specified string. To enable it, just check the "Regular Expression" checkbox in the options bar of the search bar.
![http://monkeystudio.googlecode.com/svn/wiki/images/snapshot4.png](http://monkeystudio.googlecode.com/svn/wiki/images/snapshot4.png)

### Classical Searching vs. RegExp Searching ###
The classical searching can only match the string which is the same as the search string. For example, if you search for "car" in these lines:
```
this car is a piece of cartoon. it's not a real CAAAR.
```
it'll match:
```
this "car" is a piece of "car"toon. it's not a real CAAAR.
```
in this case we only matched two occurrences, & only one of them is the one we need. Notice that the last word wasn't matched because it's not the same as the search string.<br />
To do so, we can use the RegExp, which, as we said, a logical pattern. The meaning of "logical pattern" is that we are not matching string with string, but, we are matching a string with a set of strings according to the pattern used. To write a simple pattern you need to know how the pattern is being processed. For example, this pattern "`c[a]+r[\s\W]`". The parts of these pattern are:
  * c: this is a letter, the RegExp engine will match a single c letter.
  * `[a]+`: putting a letter between the expression brackets means something special is going to be with this. In this case we are searching for a letter a one time & more.
  * r: the same as c.
  * `[\s\W]`: again, the expression brackets, but, the expression here is different, we didn't provide normal characters, we provided literal characters. These characters can mean one thing or a set of things. the \s means a space & the \W means a non-word character such as "'(/.>,:;<|.
Now let's look to the pattern we made:
  1. we asked the engine to match a string starting with c.
  1. & followed by single or multi a.
  1. & followed by r.
  1. & ends with space or a non-word character.
if we applied this pattern on the last testcase, we will get:
```
this "car" is a piece of cartoon. it's not a real "CAAAR".
```
to learn more about the patterns, refer to: http://en.wikipedia.org/wiki/Regular_expression

### Replacing with RegExp ###
As searching in RegExp is done, now, you need to benefit from the replacing feature. if you just want to replace the search pattern with a string you just need to put that string in the replace textbox, like:
![http://monkeystudio.googlecode.com/svn/wiki/images/snapshot5.png](http://monkeystudio.googlecode.com/svn/wiki/images/snapshot5.png)
if we applied that on the last example we will get:
```
this cycle is a piece of cartoon. it's not a real cycle.
```
in this case, we just replaced a pattern with a string, while, RegExp gave us the power to replace a pattern with a pattern. To do so, you need to know about the "magical brackets" or the capturing group "()". Those two brackets indicates that the part of the search pattern should be captured as a variable, for example, if we added the capturing group to the last search pattern in this way: `(c[a]+)r[\s\W]`, then, we are telling the RegExp engine to capture the found string in a variable name equals the one-based ID of the grouping capture --$1. & if we added another capturing group to the pattern to be: `(c[a]+)r([\s\W])`, then, we will have two variables --$1 & $2. Now, set the last pattern in the search textbox & `damned-$1'$2` in the replace textbox & apply that to our first example, we will have:
```
this damned-ca' is a piece of cartoon. it's not a real damned-CAAA'.
```
In this case, we are able to replace the code with a richer way.


### Notices ###
MonkeyStudio uses the [QRegExp](http://qt.nokia.com/doc/4.6/qregexp.html#details) engine for applying RegExp in Search & Replace plugin in the current version. Till now, we don't have any ideas about changing the engine, but, if we do, we will let you know.

---

(1): Integrated Development Environments.<br />
(2): Regular Expression, also known as regex.<br />