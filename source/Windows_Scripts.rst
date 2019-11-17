Scripts
=======

This window is accessible by selecting Tools > Scripting...

Use
---

The Scripting window allows you to load an existing script into the text
area and run it against the current opened project. To customize the
scripting feature, do the following:

-  Load a script into the editor by clicking its name in the list in the
   left-hand panel.

-  Right-click a button from <1> to <12> in the bottom panel and select
   Add Script.

-  When you left-click the number, the selected script will run. You can
   also start the selected macros from the main menu by using their
   entries in the Toolsmenu or by pressing Ctrl+Alt+F# (# 1 to 12).

By default, scripts are stored in the ``scripts`` folder located in the
OmegaT installation folder (the folder that contains the ``OmegaT.jar``
file).

If you add new scripts there, they will appear in the list of available
scripts in the Scripting window.

Some additional scripts can be found here: `OmegaT
Scripts <https://sourceforge.net/projects/omegatscripts/>`__

Scripting languages
-------------------

The following scripting languages have been implemented:

-  **Groovy** (http://groovy.codehaus.org): a dynamic language for the
   Java Virtual machine. It builds upon the strengths of Java but has
   additional power features inspired by languages like Python, Ruby and
   Smalltalk.

-  **JavaScript** (sometimes abbreviated JS, not to be confused with
   Java): a prototype-based scripting language that is dynamic, weakly
   typed and has first-class functions. It is a multi-paradigm language,
   supporting object-oriented, imperative, and functional programming
   styles. Being the language behind popular software such as Firefox,
   it is a familiar and preferred programming tool in the open-source
   domain.

All the languages have access to the OmegaT object model, with the
project as the top object. For example, the following Groovy code
snippet scans through all the segments in all the files in the current
project and, if a translation exists, prints out the source and the
target of the segment:

::

        files = project.projectFiles;
        for (i in 0 ..< files.size())
        {
            for (j in 0 ..< files[i].entries.size())
            {
                currSegment = files[i].entries[j];
                if (project.getTranslationInfo(currSegment))
                {
                    source = currSegment.getSrcText();
                    target = project.getTranslationInfo(currSegment).translation;
                    console.println(source + " >>>> " + target);
                }     
            }
        }
