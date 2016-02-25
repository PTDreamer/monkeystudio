# Introduction #

The regular expression editor help you to define Qt regular expressions by creating visual tree of captured texts.

# Details #

This plugin is  very easy to use, simply:

  * Fill the regular expression line edit
  * Set the regular expression options
  * Set a text to test your regular expression on
  * Click the process button (or press return in the regular expression line edit)
  * And finally check the captured texts result tree ;)

The regular expression have to be formatted accordingly to the **QRegExp** class of the Qt Framework.<br />
The editor has a built in infinite loop breaker to allow the user to stop a bad regular expression that infinitely loop.<br />
If a regular expression loop too much or take too much time, you can be query to continue or stop the process.