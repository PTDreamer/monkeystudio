# Introduction #

The MkS Shell plugin add a terminal like front end to our internal MkSShellInterpreter.

# Details #

The MkS Shell Interpreter is a command processing class that allow us to execute command on object without needing to deal directly with them.<br />
The MkS Shell plugin allow you to execute commands directly by hand.<br />
It's more a debugging / dev tool than something you may daily need.<br />
Usualy **red** output mean something went **wrong**, while something **green** mean something **right**.

## Short list of builtin commands: ##

  * [help](MkSShell#help.md): List available commands, print help for a command.
  * [echo](MkSShell#echo.md): Print back the passed parameters to the output.
  * [parser](MkSShell#parser.md): Add and remove console output parsers.
  * [abbreviation](MkSShell#abbreviation.md): Manage abbreviations - quick way for insert syntax constructions.
  * [associaton](MkSShell#association.md): Configure file name to language associations.
  * [environment](MkSShell#environment.md): Manage system environment.(i.e. set PATH for search compilers and other software)
  * [tools](MkSShell#tools.md): Add and remove tools - configurable menu items.



## Commands description: ##

---

### help ###
**NAME**
> help - list available commands, print help for a command.

**SYNOPSIS**
> help `[COMMAND]`

**DESCRIPTION**
> If executed without arguments - list all available commands.<br />
> If COMMAND name given - print help information for the command.

---

### echo ###
**NAME**
> echo - display a line of text.

**SYNOPSIS**
> echo `[STRING(s)]`

**DESCRIPTION**
> Split string(s) onto arguments, and print, how it is interpreted by interpreter. This command don't have any practical reason, but can we used for test purposes. For example - test, how does special symbols escaping work, and how arguments splited.

**EXAMPLES**
```
MkS:/> echo hello, world
Argument: <hello,>
Argument: <world>
MkS:/> echo 'hello, world'
Argument: <'hello,>
Argument: <world'>
MkS:/> echo "hello, world"
Argument: <hello, world>
MkS:/> 
```

---

### parser ###
**NAME**
> parser - allows to add and remove console output parsing patterns.

**SYNOPSIS**
> parser `[add NAME REGEXP FILENAME COLUMN ROW PATTERN_TYPE PATTERN_TEXT FULL_TEXT | remove NAME REGEXP]`

**DESCRIPTION**
> Add or remove console parsers.<br>
<blockquote>You can find info about parsers at <doxygen docs>/doc/html/parsing.html file.<br /></blockquote>

<blockquote>add - add parser. Parameters listed.<br />
remove - remove parser by it's name and regular expression.<br>
<b>EXAMPLES</b>
<pre><code>MkS:/&gt; # #warning preprocessor dirrective<br>
MkS:/&gt; parser add "GCC" "^([\w\d\./\\\-]+):(\d+):\d+: warning: #warning ([^\n]*)" "%1" "-1" "%2" "warning" "%3" "%0"<br>
</code></pre>
<hr />
<h3>abbreviation</h3>
<b>NAME</b>
abbreviation - Manage abbreviations (<b>code snipets</b>) - quick way for insert syntax constructions.</blockquote>

<b>SYNOPSIS</b>
<blockquote>abbreviation <code>[add MACRO DESCRIPTION LANGUAGE CODE | del MACRO LANGUAGE | show MACRO LANGUAGE | list &lt;LANGUAGE&gt; | clear]</code></blockquote>

<b>DESCRIPTION</b>
<blockquote>Add, delete, show, list or clear abbreviations, some templates can be show <a href='http://monkeystudio.org/wiki/Abbreviations'>here</a>.<br />
A place holder (<b>'|'</b> character) can be inserted to state where the text cursor should be positioned after the macro expansion.<br /></blockquote>

<blockquote>add - Add an abbreviation.<br />
del - Delete a specific language macro.<br />
show - Show a specific language macro.<br />
list - List all abbreviations of a specified language, or all languages if language is not specified.<br />
clear - clear all abbreviations</blockquote>

<b>EXAMPLES</b>
<pre><code>MkS:/&gt; abbreviation add "switchb" "A switch statement" "C++" "switch( | )\n{\n}"<br>
MkS:/&gt; <br>
</code></pre>
<hr />
<h3>association</h3>
<b>NAME</b>
<blockquote>association - Manage associations (<b>languages suffixes</b>) - quick way for associate some file extension with language names.</blockquote>

<b>SYNOPSIS</b>
<blockquote>association <code>[add TYPE SUFFIXES | set TYPE SUFFIXES | del TYPE SUFFIXES | list &lt;TYPE&gt; | clear &lt;TYPE&gt;]</code></blockquote>

<b>DESCRIPTION</b>
<blockquote>Add, set, delete, list or clear associations.<br /></blockquote>

<blockquote>add - Add associations (previous content is keep).<br />
set - Set associations (previous content is erased).<br />
del - Delete a specific language associations.<br />
list - List all associations of a specified language, or all languages if language is not specified.<br />
clear - clear all associations or the language associations if defined.</blockquote>

<b>EXAMPLES</b>
<pre><code>MkS:/&gt; association set "C++" "*.c, *.cpp, *.h, *.hpp"<br>
MkS:/&gt; <br>
</code></pre>
<hr />
<h3>environment</h3>
<b>NAME</b>
<blockquote>environment - Manage environment variables - quick way for manage environment variables inside MkS.</blockquote>

<b>SYNOPSIS</b>
<blockquote>environment <code>[set NAME VALUE | unset NAME | clear | enable NAME true/false | list]</code></blockquote>

<b>DESCRIPTION</b>
<blockquote>Set, unset, clear, enable or list environment variables.<br /></blockquote>

<blockquote>set - Set the content of a variable.<br />
unset - Unset the content of a variable.<br />
clear - Unset all variables.<br />
enable - Enable or disable a variable. A disable variable will not be defined when running a process.<br />
list - List all variables and their value.</blockquote>

<b>EXAMPLES</b>
<pre><code>MkS:/&gt; environment set "PATH" "/usr/bin"<br>
MkS:/&gt; environment enable "PATH" "false"<br>
MkS:/&gt;<br>
</code></pre>
<hr />
<h3>tools</h3>
<b>NAME</b>
<blockquote>tools - Manage tools inside MkS menu bar - quick way for add custom actions in the MkS menu bar.</blockquote>

<b>SYNOPSIS</b>
<blockquote>tools <code>[set CAPTION ICON FILEPATH WORKING_PATH DESKTOP_ENTRY(true/false) USE_CONSOLE_MANAGER(true/false) | unset CAPTION | clear | update-menu | list]</code></blockquote>

<b>DESCRIPTION</b>
<blockquote>Set, unset, clear, update menu or list tools.<br /></blockquote>

<blockquote>set - Set a tool.<br />
unset - Unset a tool.<br />
clear - Unset all tools.<br />
update-menu - Update (apply) the menu bar entries.<br />
list - List all tools and their properties.</blockquote>

<b>EXAMPLES</b>
<pre><code>MkS:/&gt; tools set "Calculator" "calc.png" "calc.exe" "" "false" "false"<br>
MkS:/&gt; tools update-menu<br>
MkS:/&gt; tools list<br>
MkS:/&gt; tools clear<br>
MkS:/&gt; tools update-menu<br>
</code></pre>
<hr />