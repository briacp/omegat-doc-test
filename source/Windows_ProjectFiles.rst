Project Files
=============

This window is displayed automatically when OmegaT loads a project, and
at any time by pressing Project > Project Files....

Note: it is possible to inhibit the window displaying at opening, by
setting *project\_files\_show\_on\_load* to *false* in ``omegat.prefs``
file (accessible by Options > Access Configuration Folder menu).

Use Ctrl+L to open and Esc to close it. The Project Files Window
displays the following information:

-  the total number of translatable files in the project. These are the
   files present in the /source folder in a format that OmegaT is able
   to recognize. This number is displayed in brackets, next to the
   "Project file" title

-  the list of all translatable files in the project. Clicking on any
   file will open it for translation.

   Typing any text will open a Filter field where parts of filenames can
   be entered. You can select a file with Up and Down keys, and open it
   for translation by pressing Enter

   Note: filenames (in first column) can be sorted alphabetically by
   clicking in the header. It also possible to change the position of a
   filename, by clicking on it and pressing *Move ...* buttons.

   Right-clicking on a filename opens a popup that allows to open the
   source file and (if it exists) the target file.

-  File entries include their names, file filter types, their encoding
   and the number of segments each file contains

-  the total number of segments, the number of unique segments in the
   whole project, and the number of unique segments already translated
   are shown at the bottom

The set of **Unique**\ segments is computed by taking all the segments
and removing all duplicate segments. (The definition of “unique” is
case-sensitive: "Run" and "run" are treated as being different)

The difference between "Number of segments" and "Number of unique
segments" provides an approximate idea of the number of repetitions in
the text. Note however that the numbers do not indicate how relevant the
repetitions are: they could mean relatively long sentences repeated a
number of times (in which case you are fortunate) or it could describe a
table of keywords (not so fortunate). The ``project_stats.txt`` located
in the omegat folder of your project contains more detailed segment
information, broken down by file.

Modifying the segmentation rules may have the effect of modifying the
number of segments/unique segments. This, however, should generally be
avoided once you have started translating the project. See the chapter
*Segmentation rules* for more information.

**Adding files to the project:**\ You can add source files to the
project by clicking on the "Import Source Files..." button. This copies
the selected files to the ``source`` folder and reloads the project to
import the new files. You can also add source files from Internet pages,
written in MediaWiki, by clicking on"Import from MediaWiki" button and
providing the corresponding URL.
