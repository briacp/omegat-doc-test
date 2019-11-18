Installing and running OmegaT
#############################

Windows Users
*************

Downloading the package
=======================

Do you have a Java implementation compatible with Oracle's Java 8 JRE?

-  **Yes:**\ download ``OmegaT_4.n.n_Windows_without_JRE.exe``.

-  **No / I don't know:** download ``OmegaT_4.n.n_Windows.exe``.

   This package is bundled with Oracle's Java Runtime Environment. This
   JRE will not interfere with other Java implementations that may
   already be installed on your system.

Installing OmegaT
==================

To install OmegaT, double-click on the program you have downloaded.

At the beginning of the installation you can select the language to be
used during the installation. In the following window you can indicate
that the language selected is to be used in OmegaT. If you check the
corresponding checkbox, the ``OmegaT.l4J.ini`` file is modified to use
the language selected (see next section for details). Later, after you
have accepted the license agreement, the setup program asks you whether
you wish to create a folder in the *Start* menu, and whether you wish to
create a shortcut on the desktop and in the quick launch bar - you can
create these shortcuts later by dragging ``OmegaT.exe`` to the desktop
or to the Start menu to link it from there. The last frame offers you to
have a look at the readme and changes files for the version you have
installed.

Running OmegaT
==============

Once OmegaT is installed, you can click on ``OmegaT.jar`` to launch it
directly or you can launch it directly from the command line.

The simplest way to launch OmegaT, however, is to execute the
``OmegaT.exe`` program. The options for the program start-up in this
case will be read from the ``OmegaT.l4J.ini`` file, which resides in the
same folder as the exe file and which you can edit to reflect your
setup. The following example for the INI file reserves 1 GB of memory,
requests French as the user language and Canada as the country:

::

    # OmegaT.exe runtime configuration
    # To use a parameter, remove the '#' before the '-'
    # Memory
    -Xmx1024M
    # Language
    -Duser.language=FR
    # Country
    -Duser.country=CA

.. hint:: If OmegaT works slowly in Remote Desktop sessions under Windows, you may use this option:
  ::
    -Dsun.java2d.noddraw=false

Upgrading OmegaT
================

*This information applies only to the "Traditional" Windows versions of
OmegaT. It does not apply to the Web Start versions, which are upgraded
automatically, nor to cross-platform versions installed on Windows.*

If you already have a version of OmegaT installed on your PC and wish to
upgrade to a more recent version, you have two options:

-  **Install over the existing installation.** To do this, simply select
   the same installation folder as the existing installation when
   installing the new version. The "old" version of OmegaT will be
   overwritten, but any settings from it will be retained. This includes
   preferences set from within OmegaT, any changes you have made to your
   ``OmegaT.l4J.ini`` file, and also your launch script (``.bat`` file),
   if you are using one.

With this method, you may also download the "Windows without JRE"
version, since the new installation will use your existing JRE.

-  **Install to a new folder.** This will enable you to keep both
   versions side-by-side, which you may wish to do until you feel
   comfortable with the new version. This method will also use
   preferences and settings you have made from within OmegaT. In this
   case, however:

   -  If you have made changes to your ``OmegaT.l4J.ini`` file and/or
      are using a .bat file, you must copy these over.

   -  If your existing OmegaT installation is a "Windows with JRE"
      version, the new version must also be a "Windows with JRE"
      version.

Linux (Intel) Users
*******************

Downloading the right package for Linux
=======================================

Do you have a Java implementation compatible with Oracle's Java 8 JRE?

-  **Yes:**\ download ``OmegaT_4.n.n_Without_JRE.zip``.

-  **No / I don't know:** download ``OmegaT_4.n.n_Linux.tar.bz2``.

   This package is bundled with Oracle's Java Runtime Environment. This
   JRE will not interfere with other Java implementations that may
   already be installed on your system.

Installing OmegaT on Linux
==========================

Unpack/untar the downloaded file. This will create an ``omegat/`` folder
in the working folder in which you will find all the files needed to run
OmegaT. To untar the ``.tar.gz`` file:

::

    $ tar xf downloaded_file.tar.gz

Adding OmegaT to your menus (KDE) or panels (Gnome)
---------------------------------------------------

KDE 4 Users
~~~~~~~~~~~

You can add OmegaT to your menus as follows:

-  Press **Alt+F2** to show KRunner. Type *kmenuedit+enter* to run the
   command. The KMenuEditor appears. In KMenuEditor select *File > New
   Item.*

-  Then, after selecting a suitable menu, add a submenu/item with *File
   - New* Submenu and *File - New Item*. Enter OmegaT as the name of the
   new item.

-  In the "Command" field, use the navigation button to find your OmegaT
   launch script (the file named OmegaT in the unpacked folder), and
   select it.

-  Click on the icon button (to the right of the
   Name/Description/Comment fields)

-  Other Icons - Browse, and navigate to the ``/images`` subfolder in
   the OmegaT application folder. Select the ``OmegaT.png`` icon.

-  Finally, save the changes with *File - Save.*

GNOME Users
~~~~~~~~~~~

You can add OmegaT to your menus as follows:

-  Right-click on the panel - *Add New Launcher*.

-  Enter "OmegaT" in the "Name" field; in the "Command" field, use the
   navigation button to find your OmegaT launch script (the file named
   OmegaT in the unpacked folder). Select it and confirm with OK.

-  Click on the icon button, then hit Browse... and navigate to the
   ``/images`` subfolder in the OmegaT application folder. Select the
   ``OmegaT.png`` icon. GNOME may fail to display the icon files in the
   available formats and initially appear to expect an SVG file, but if
   the folder is selected, the files should appear and ``OmegaT.png``
   can be selected.

Running OmegaT on Linux
=======================

You can launch OmegaT from the command line with a script that includes
start-up options or you can click on ``OmegaT.jar`` to launch it
directly. Methods differ depending on the distribution. Make sure that
your ``PATH`` settings are correct and that ``.jar`` files are properly
associated with a Java launcher. Check "Command line launching" below
for more information.

macOS Users
***********

Downloading the package for macOS
=================================

OmegaT contains the Java JRE 1.8

Download ``OmegaT_4.n.n_Mac.zip``.

Installing OmegaT on macOS
--------------------------

Double click on ``OmegaT_4.n.n_Mac.zip`` to unpack it. This creates a
folder called ``OmegaT``. The folder contains 2 files: ``index.html``
and ``OmegaT.app``. Copy the folder to a suitable folder (e.g.
Applications). Once you have done this, you can delete the
``OmegaT_4.n.n_Mac.zip`` file, it is no longer needed.

Adding OmegaT to the Dock
-------------------------

Drag and drop ``OmegaT.app`` onto the Dock.

Running OmegaT on macOS
-----------------------

Double-click on ``OmegaT.app`` or click on its location in the Dock.

You can modify OmegaT's behaviour by editing the *Properties* as well as
the ``Configuration.properties`` file in the package.

To access ``Configuration.properties``, right-click on ``OmegaT.app``
and select "Show Package Contents", then open the file in
``Contents/Resources`` by right-clicking on it and selecting your text
editor of choice. You can also ``cd`` there directly from the command
line and open ``Configuration.properties`` in a command line editor like
emacs or vi.

Options are changed by modifying ``Configuration.properties``. For
pre-defined options, remove the ``#`` before a parameter to enable it.
For example, ``user.language=ja`` (without the ``#``) will launch OmegaT
with the user interface in Japanese.

To change the amount of memory available, edit
*OmegaT.app/Contents/Info.plist* file and un-comment the line
``<!-- <string>-Xmx6g</string> -->`` by removing the ``<!--`` and ``-->``.
This will launch OmegaT with 6GB of memory; change the ``6g`` to the desired amount.

To launch multiple instances of ``OmegaT.app``, double-click the file
*OmegaT* located in ``OmegaT.app/Contents/MacOS/``.

Use the ``OmegaT.jar`` file located in
``OmegaT.app/Contents/MacOS/Java/`` to launch OmegaT from the command
line. Check "Command line launching" below for more information.

macOS goodies
-------------

``OmegaT.app`` can make use of macOS Services. You can thus select a
word anywhere in OmegaT and use Services to check this word, for
instance in Spotlight or in Google. You can also use AppleScript or
Automator to create Services or scripts that will automate frequent
actions.

Other Systems
*************

This information applies to systems such as Solaris SPARC/x86/x64, Linux
x64/PowerPC, Windows x64.

Downloading the right package
=============================

OmegaT is available bundled with a Oracle Java JRE for Linux (Intel x86)
and Windows platforms. Users of other platforms (Linux PowerPC, Linux
x64, Solaris SPARC/x86/x64, Windows x64 etc) must have a running
compatible Java JRE on their system to be able to use OmegaT.

Do you have a Java implementation compatible with Oracle's Java 8 JRE?

-  **Yes:** download ``OmegaT_4.n.n_Windows_without_JRE.zip``. This
   package can be used on any platform where a Java 8 compatible JRE is
   installed.

-  **I don't know:** open a terminal and type ``java -version``. If a
   "command not found" or similar message is returned, it is likely that
   Java is not installed on your system.

-  **No:** obtain a Java JRE for your system (see below) and download
   ``OmegaT_4.n.n_Without_JRE.zip``.

   Oracle provides JREs for Solaris SPARC/x86 (Java 8) and for Linux
   x64, Solaris x64, Windows x64 (Java 8) at
   `<http://www.oracle.com/technetwork/java/archive-139210.html>`__.

   IBM provides JREs for Linux PowerPC at
   `<http://www.ibm.com/developerworks/java/jdk/linux/download.html>`__.

   Follow the installation instructions of the package you need.

Installing OmegaT on other systems
==================================

To install OmegaT, simply unpack the ``OmegaT_4.n.n_Without_JRE.zip``
file. This creates an ``./OmegaT_4.n.n_Without_JRE/`` folder in the
working folder with all the files necessary to run OmegaT.

Installing convenient shortcuts
-------------------------------

Follow your system's instructions to install OmegaT shortcuts in
convenient places of your choosing.

Running OmegaT on other systems
===============================

Once OmegaT is installed, you can launch it directly from the command
line, you can create a script that includes launch parameters for the
command line or you can click on ``OmegaT.jar`` to launch it directly.
Methods differ depending on the distribution. Make sure that your
``PATH`` settings are correct and that ``.jar`` files are properly
associated with a Java launcher. Check "Command line launching" below
for more information.

Drag and drop
*************

In most systems, it is possible to open a project by dropping an
``omegat.project`` file onto the OmegaT icon on the desktop. It might
also be possible to open an OmegaT project by double-clicking on an
``omegat.project`` file.

Using Java Web Start
********************

Java Web Start technology (part of Java 8 and above) can be used to
deploy standalone Java software applications with a single click over
the network. Java Web Start ensures that the latest version of the
application will be deployed, as well as the correct version of the Java
Runtime Environment (JRE) used. To start OmegaT for the first time with
Java Web Start, load the following URL in your browser:

` <https://omegat.sourceforge.io/webstart/OmegaT.jnlp>`__

Download the file ``OmegaT.jnlp`` and then click on it. During the
installation, depending on your operating system, you may receive
several security warnings. The permissions you give to this version
(which may appear as "unrestricted access to the computer") are
identical to the permissions you give to the local version, i.e., they
allow access to the hard drive of the computer. Subsequent clicks on
``OmegaT.jnlp`` will check for any upgrades, install them, if there are
any, and then start OmegaT. After the initial installation you can, of
course, also use ``OmegaT.jnlp`` also when you are offline.

**Privacy**: OmegaT Java Web Start does not save any of your information
beyond the computer on which you are running it. The application runs on
your machine only. Your documents and translation memories remain on
your computer, and the OmegaT project will have no access to your work
or information.

Note that if you need or wish to use any of the launch command arguments
(see above), you must use the normal installation.

Starting OmegaT from the command line
*************************************

Normally, it is not necessary to start OmegaT from the command line.
However, the command-line alternative allows the user to control and
modify the program's behavior. There are two ways of launching OmegaT
using the command line.

Opening a command line window
=============================

A command line window is also referred to as a "terminal window". On
Windows it is called an "MS-DOS window" and is available from the Start
Menu, inside Programs, through the "MS-DOS" item. The macOS equivalent
is the application Terminal located in ``Applications/Utilities``.

To launch OmegaT, you must normally type two commands. The first of
these is:

::

    cd folder

where ``folder`` is the name of the folder, with complete path, in which
your OmegaT program - specifically, the file ``OmegaT.jar`` - is
located. In practice, this command will therefore be something like
this:

On Windows

::

    cd C:\Program Files\OmegaT

On macOS

::

    cd <OmegaT.app location>/OmegaT.app/Contents/Resources/Java/

On Linux

::

    cd /usr/local/omegat

This command changes the folder to the folder containing the executable
OmegaT file. The second command is the command which actually launches
OmegaT. In its most basic form, this command is:

::

    java -jar OmegaT.jar

Pay attention to the capitalization - in OS other than Windows, the
program will not start, if you enter ``omegat`` instead of ``OmegaT``!

This method has a particular benefit of being suitable for finding
causes of problems: if an error occurs during use of the program, an
error message is output in the terminal window which may contain useful
information on the cause of the error.

The above method somewhat impractical way of launching a program
routinely. For this reason, the two commands described above are
contained in a file (a "script", also called a "``.bat`` file" on
Windows systems).

When this file is executed, the commands within it are automatically
carried out. Consequently, to make changes to the launch command, it is
sufficient to modify the file.

Launch command arguments
========================

The basic command has already been mentioned above. Changes to this
command involve the addition of "arguments" to it. Arguments are added
after the initial ``java``, and before the ``-jar OmegaT.jar``. Note that in Windows you can change the
``OmegaT.l4J.ini`` file to reflect your preferences. In other platforms,
you can modify ``Configuration.properties`` file on the Mac, or
``OmegaT`` launcher under Linux to do the same.

A list of possible arguments is given below. Advanced users can obtain
more information on the arguments by typing *man java* in the terminal
window.

-  **User interface language**

   **-Duser.language=XX** Normally, i.e. when OmegaT is launched
   without any arguments, the program first detects the language of the
   user's operating system. If a user interface in this language is
   available, OmegaT uses it. So, if the user's operating system is
   Russian and OmegaT has been localized in Russian, OmegaT is displayed
   with a Russian user interface, Russian menus, etc. If the language of
   the user's system is not available, OmegaT defaults to English. This
   is the standard behavior.

   The ``-Duser.language=XX`` argument causes OmegaT to use the language
   specified rather than the language of the user's operating system.
   ``XX`` in the command stands for the two-digit code of the desired
   language. To launch OmegaT with a French interface (for example on a
   Russian operating system), the command would therefore be:

   ::

       java -Duser.language=fr -jar OmegaT.jar

-  **User country**

   **-Duser.country=``XX``** Besides the language, you can also specify
   the country, for example ``CN`` or ``TW`` in case of the Chinese
   language. To display the instant start guide in the desired language,
   you need to specify both the language and the country. This is
   necessary even if there's only one combination available, like
   ``pt_BR`` in case of Brazilian Portuguese.

-  **Memory assignment**

   **``-Xmx??M``**\ This command assigns more memory to OmegaT. By
   default, 1024 MB are assigned, so there is no advantage in assigning
   less than this figure. ``??`` stands for the amount of memory
   assigned, in megabytes. The command to launch OmegaT with assignment
   of 2048 MB (2 GB) of memory is therefore:

   ::

       java -Xmx2048M -jar OmegaT.jar

-  **Proxy host IP address**

   **``-Dhttp.proxyHost=nnn.nnn.nnn.nnn``** The IP address of your proxy
   server, if your system uses a proxy.

-  **Proxy host port number**

   **``-Dhttp.proxyPort=NNNN``** The port number your system uses to
   access the proxy server.

-  **Google Translate V2**

   **``-Dgoogle.api.key=A123456789B123456789C123456789D12345678``** If
   you have signed up for the Google Translate services, enter your
   private Google API key here. Note that the key is 38 characters long.

-  **Microsoft Translator**

   Make sure that you have a free Microsoft account. You’ll need this to
   sign-in to `Windows Azure
   Marketplace <http://datamarket.azure.com/dataset/bing/microsofttranslator#schema>`__
   and use the Translator service. Note that up to 2M characters per
   month are free of charge. The two entries required are available in
   your `account page <https://datamarket.azure.com/account>`__ under
   Primary account key and Customer-ID:

   ::

       -Dmicrosoft.api.client_id=XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX

   ::

       -Dmicrosoft.api.client_secret=XXXX9xXxX9xXXxxXXX9xxX99xXXXX9xx9XXxXxXXXXX=

-  **Yandex Translate**

   Make sure that you have a free Yandex account. You’ll need this to be
   able to obtain and use Yandex Translate API key. API keys can be
   requested using `API key request
   form <http://api.yandex.com/key/form.xml?service=trnsl>`__, and
   viewed on `My Keys <http://api.yandex.com/key/keyslist.xml>`__ page.

   ::

       -Dyandex.api.key=trnsl.1.1.XXXXXXXXXXXXXXXX.XXXXXXXXXXXXXXXX.XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Arguments can be combined: to launch OmegaT with all the examples
described above, the command would be:

::

    java -Dswing.aatext=true -Duser.language=pt -Duser.country=BR -Xmx2048M -Dhttp.proxyHost=192.168.1.1 -Dhttp.proxyport=3128 -jar -OmegaT.jar

OmegaT in the command line mode
-------------------------------

The purpose of the console mode is to use OmegaT as a translation tool
in a scripting environment. When started in console mode, no GUI is
loaded (so it will work on any console) and the given project is
automatically processed as requested.

Prerequisites
~~~~~~~~~~~~~

To run OmegaT in the command line mode, a valid OmegaT project must be
present. The location does not matter, since you have to add it to the
command line at the start-up anyway.

If you need altered settings, the configuration files must be available.
This can be achieved in two ways:

-  Run OmegaT normally (with the GUI) and specify the settings. If you
   start OmegaT in console mode, it will use the same settings.

-  If you can't run OmegaT normally (no graphical environment
   available): copy the settings files from some other OmegaT
   installation on another machine to a specific folder. The location
   does not matter, since you can add it to the command line at startup.
   The relevant files are ``filters.conf`` and ``segmentation.conf`` and
   can be found in the user home folder (e.g. ``C:\Documents and Settings\user\OmegaT`` under Windows, ``~/.omegat/`` under Linux).

Starting in console mode
~~~~~~~~~~~~~~~~~~~~~~~~

To start OmegaT in console mode, some extra parameters have to be passed
to it on startup. The most important is ``/path/to/project``, and
optionally ``--config-dir=/path/to/config-files/``. Example:

::

    java -jar OmegaT.jar /path/to/project \
        --config-dir=/path/to/config-files/ \
        --config-file=/path/to/config-file/ \
        --mode=console-translate|console-createpseudotranslatetmx|console-align \
        --source-pattern=regexp

Note that all parameters start with a double ``-`` character.

**Explanation:**

-  ``/path/to/project`` tells OmegaT where to find the project to
   translate. If given, OmegaT starts in console mode and will translate
   the given project.

-  ``--config-dir=/path/to/config-files/`` tells OmegaT in which folder
   the configuration files are stored. If not given, OmegaT reverts to
   default values (OmegaT folder under user home or, if unavailable, the
   current working folder). Note the double ``-`` character.

-  ``--config-file=/path/to/config-file/`` tells OmegaT what
   configuration file to use.

-  *``--mode=...``* OmegaT starts in console mode to perform one of the
   following services automatically

   -  *``--mode=console-translate``*

      In this mode, OmegaT will attempt to translate the files in
      ``/source/`` with the available translation memories. This is
      useful to run OmegaT on a server with TMX files automatically fed
      to a project.

   -  ``--mode=console-createpseudotranslatetmx``

      In this mode OmegaT will create a TMX for the whole project, based
      on the source files only. You specify the TMX file to be created
      with

      ``--pseudotranslatetmx=allsegments.tmx --pseudotranslatetype=equal|empty``

      The argument *pseudotranslatetype* specifies, whether the target
      segments are to be equal to the source, or left empty.

   -  ``--mode=console-align``

      In this mode, OmegaT will align the Java properties files found in
      the ``/source/`` folder of the project to the contents found at
      the specified location. The resulting TMX is stored in the
      ``/omegat/`` folder under the name ``align.tmx``.

      Additional parameter is required in this case, specifying the
      location of the target data:

      ``--alignDir=<location of translated files>``

      ``alignDir`` must contain a translation in the target language of
      the project. For instance, if the project is EN-to-FR,
      ``alignDir`` must contain a bundle ending with ``_fr``. The
      resulting TMX is stored in the ``omegat`` folder under the name
      ``align.tmx``.

-  ``--source-pattern=regexp``

   When mode has been used, this option will specify the files to be
   processed automatically. If the parameter is not specified, all files
   will be processed. Here's few typical examples to limit your choice:

   -  ``.*\.html``

      All HTML files will be translated - note that the period in the
      usual ``*.html`` has to be escaped (``\.``) as specified by the
      rules for regular expressions

   -  ``test\.html``

      Only the file test.html at the root of the source folder will be
      translated. If there are other files named test.html in other
      folders, they will be ignored.

   -  ``dir-10\\test\.html``

      Only the file ``test.html`` in the folder ``dir-10`` will be
      processed. Again note that the backslash is escaped as well.

-  ``--tag-validation=abort|warn`` ``outputFileName``

   This option allows the tag validation in a batch mode. If ``abort``
   is selected, the tag validator will stop on the first invalid
   segment. If ``warn`` is specified, the tag validator will process all
   segments and write warnings about any segments with invalid tags into
   the file specified.

-  ``--no-team`` addresses projects set up for team work. Use it if
   OmegaT is not to synchronize the project contents.

-  ``--disable-project-locking`` allows, under Windows, to open the same
   project with several instances of OmegaT. By default, under Windows,
   ``omegat.project`` is locked, and an error message is received when
   trying to open a project already opened in another instance of
   OmegaT. With that option, no locking occurs.

Quiet option
~~~~~~~~~~~~

An extra command line parameter specific to console mode: ``--quiet``.
In the quiet mode, less info is logged to the screen. The messages you
would usually find in the status bar are not displayed.

Usage: ``java -jar OmegaT.jar /path/to/project --mode=console-translate --quiet``

Building OmegaT From Source
===========================

The sources of the current version can be retrieved with a SVN client
from the repository `svn://svn.code.sf.net/p/omegat/svn/trunk <svn://svn.code.sf.net/p/omegat/svn/trunk>`_ or
directly on
`SourceForge <https://sourceforge.net/p/omegat/svn/HEAD/tarball?path=/trunk>`_.

Once the code is downloaded, open a command in the source folder and
type:

::

    gradlew assembleDist

This will create a full distribution of OmegaT in the
``./build/distributions`` folder, where you will find a zip containing
everything needed to run OmegaT.

You can also run directly the application with the following command:

::

    gradlew run

Detailed instructions on building are in the docs\_devel
`readme <https://sourceforge.net/p/omegat/svn/HEAD/tree/trunk/docs_devel/README.txt>`__.
