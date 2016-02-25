# Introduction #

The tools plugin allows you to add to a pre-created menu by the plugin, a set of commands a user can define & a set of external programs, so that the accessibility to the often used tools becomes easier.<br />
The plugin have some [Mks Shell](MkSShell.md) commands you can use, see [here](MkSShell#tools.md).

# User Tools #

> You can configure **User Tools** triggering the "**Tools > Edit User Tools**" action.

  * To add a new tool, simply press the add button and fill parameters:
    * **Caption**: The visible text the command will appear with in the menu bar.
    * **File Path**: The file path of a binary or document file. Parameters can be added here too.
    * **Working Path**: The working path from where the command will be started.
    * **Execute using console manager**: If checked, the command will be executed inside MkS console manager meaning you will be able to see the output of the application directly in MkS.
> > An icon can be defines by click the button right of the **Caption** line edit, additionally you can also drop a picture file on the button.<br />
> > File and working path can be selected easily by clicking the button placed to their respective right.<br />
> > The second button on the **File Path** area try to update **Working Path** according to the file path absolute path.

# Desktop Tools #


> You can configure **Desktop Tools** triggering the "**Tools > Edit Desktop Tools**" action.<br />
> To make menu entries visible, simply move them to the right using a double click on items or selecting them then pressing ">>" button.<br />
> The menu entries can be filtered according to "**Filter Name**" and "**Filter Category**" so it become easy to found entries.<br />
> The right list can be ordered easily so you can add the tools in the menu sorted as you want.<br />

**NOTE 1**: "**Filter Category**" is only available on **Linux**.<br />
**NOTE 2**: As there is no concept of "**Menu Entries**" on **Mac OS X** we mimic that by using the installed applications in the **/Applications** folder.