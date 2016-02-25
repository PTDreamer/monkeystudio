# Introduction #

The Project Headers plugin allow you to (re)generate the headers of your source code (c++, html, ...).

# Details #

To use it you have to trigger the "**Edit > Project Licensing**" action.<br />
Before filling the requested fields and pressing apply, you may have a look at the different tabs:

  * **License Configuration**: This allow you to defines templates for specific languages.
    * Be careful with the regular expression, it's used to detect the existing header in files,<br />so bad regular expression can result to data lost: **BE VERY CAREFUL & BACKUP YOUR DATA FIRST**.
  * **File Encoding**: You can define the text codec to use to open / write your data when doing the headers replace.

The current handled variables for headers are:

  * **editor\_version\_string**: This is the complete ide name and version.
  * **authors**: The authors of the source code.
  * **projectname**: The project name.
  * **filename**: The source code file name.
  * **date**: The current data / time in ISO format.
  * **license**: The license of the source code.
  * **comment**: A comment you want to add.
  * **homepage**: The homepage of the project.

Some variables are handled directly by the plugin and have not to be filled but can be used in the templates, it's the case for:

  * **editor\_version\_string**
  * **filename**
  * **date**