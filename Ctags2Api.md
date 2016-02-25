# Introduction #

The Api File Generator plugin help you to generate `*`.api files needed by the QScintilla editor to provide auto completion.<br />
It's based on Ctags for extracting tags then converted to plain text api file.

# Details #

You have to have the exuberant ctags binary available on your system for the plugin to works.<br />
To create an api file, trigger the "**Edit > Api File Generator**" action.<br />
From that you have some things to fill like;

  * ctags binary: The ctags binary used to generate a tag file.
  * generate from:
    * include path: the folder you want to create api from.
    * ctags file: If you already have a tags file, you can create api from this file directly.
  * Source path: If you create the api fle from a ctags file, you may fill the base path from where the tags where indexed.
  * Remove private: Check it if you want to remove the private members from the final api file.
  * Windows Mode: check it if you are indexing windows api that contains unicode/non unicode members.
    * A: Keep members ending with A.
    * W: Keep members ending with W.

Once all is correctly filled, just click the Ok button and wait ;)<br />
After that you have to update the MkS settings through "**Edit > Settings > Source API**" and add the generated api file to the correct lexer.

You can download ctags on the official homepage at http://ctags.sourceforge.net.