#Building & Installing MkS

# Building & Installing MkS<sup>(1)</sup> #
MkS, as mentioned in the introduction, is an open-source IDE<sup>(2)</sup>. that means you can get the complete source code for it & build it on your machine alone, or you can go for the other choice, deliver it hot --or BIN!!.<br />


# Building MonkeyStudio #
let's have a quick prevision about the building process:
  * Get the source code.
  * Get MkS dependencies.
  * Build the source code.
  * enjoy MkS!!

## Get the source code ##
In fact, the MkS source code is everywhere, you can find it at the biggest source code place -- SourceForge<sup>(3)(4)</sup>, you can find it at Google Code<sup>(5)</sup> & you can find it at MonkeyStudio official website<sup>(6)</sup>.<br />
While all this places contains the different versions, we advise you to visit MkS official website to get the last news about the latest versions & the links from Google Code to download them.<br />
For instance, our last version is: 1.8.4.0b2, & you can download it from the next link:<br />
http://monkeystudio.googlecode.com/files/mks_1.8.4.0b2-svn3482-src.tar.gz<br />

The other way to get the source code, & this is what we like you to do, is to get it from the SVN<sup>(7)</sup> repository, you can follow this page to get the complete information about our SVN repository & the instructions to get the last revision from it.<br />

### SVN benefits ###
SVN repository is almost daily modified, thus, it will include the last updates & bugfixes which could be found at the packages which aren't daily modified.<br />
For standard user, we recommend the monthly revised revision which can be found at the trunk of the repository. This revision is revised twice, so, it will be in almost bugs-free revision. Again, for more information about SVN, please, follow this link.<br />

## Get MkS dependencies ##
This step varies from one operating System to another. here, we won't talk a lot, because IT VARIES.<br />

### Operating systems instructions ###
#### Gnu/Linux<sup>(R)</sup> operating systems ####
For Gnu/Linux<sup>(R)</sup>, in standard, you need to build each dependency alone, then you'll be able to build MkS in its latest version, but as long as you are using a Gnu/Linux<sup>(R)</sup> distro<sup>(8)</sup> that comes with a packages manager you'll just need to use that packages manager to install all needed packages as they are very common, & they should be available in all Gnu/Linux different distros repositories.<br />

#### Apple<sup>(R)</sup> Mac<sup>(R)</sup> OS X operating systems ####
Most of the needed dependencies can be found as binaries for Mac<sup>(R)</sup> OS X in the internet, especially at SourceForge. --just search for them.

#### Microsoft<sup>(R)</sup> Windows<sup>(R)</sup> operating systems ####
Again: Most of the needed dependencies can be found as binaries for Windows<sup>(R)</sup> in the internet, especially at SourceForge. --again, just search for them.

### Dependencies list ###
this is our list of dependencies:
  * Qt V4.4 at least.
  * QScintilla.
  * PyQt4<sup>(9)(10)</sup>.
  * PHP-Qt<sup>(11)</sup>.


---

(1): MonkeyStudio.<br />
(2): Integrated Developing Environment.<br />
(3): http://sourceforge.net/projects/monkeystudio<br />
(4): we does use SourceForge as a mirror only now.<br />
(5): http://code.google.com/p/monkeystudio<br />
(6): http://www.monkeystudio.org<br />
(7): Subversion, a version control system. http://subversion.tigris.org<br />
(8): Distribution, a Gnu/Linux modified operating system model.<br />
(9): Optional dependency, you'll need it if you'll use MkS to write PyQt projects.<br />
(10): The version should be as the same as Qt version.<br />
(11): Optional dependency, you'll need it if you'll use MkS to write PHP-Qt projects.<br />