Panes
=====

The main window consists of several panes, the main menu and a status
bar. You can change the position of any pane or even undock it to a
separate window by clicking and dragging the pane by its name. Depending
on the pane status, different signs can appear at its top right corner:

    **Note**

    If you can not see all the panes (be it opened or minimized),
    pressing Options > Restore Main Windowwill restore them to the
    state, defined in the installation.

+------------+----------------------------------------------------------------------------------+
| |image0|   | minimizes the pane, so that only its name is shown at the bottom of the window   |
+------------+----------------------------------------------------------------------------------+
| |image1|   | maximizes the pane                                                               |
+------------+----------------------------------------------------------------------------------+
| |image2|   | restores the layout before the maximizing step                                   |
+------------+----------------------------------------------------------------------------------+
| |image3|   | undocks the pane from the main window                                            |
+------------+----------------------------------------------------------------------------------+
| |image4|   | puts the pane back within the main window                                        |
+------------+----------------------------------------------------------------------------------+

Table: Pane widgets

You can overlap panes if desired. When this is done the panes display a
tab at the top. The separators between the panes can be dragged to
resize panes. Should you lose track of your changes to the user
interface, you can use Options → Restore the main window any time to
return to the original layout.

It is possible to drag and drop files to each pane, which will react
accordingly.

-  Editor pane: If an OmegaT project file (``omegat.project``) is
   dropped on this pane, the corresponding project will be opened,
   closing first any opened project. Other dropped files will be copied
   to the ``source`` folder. This applies also to the `Project files <#windows.projectfiles>`__ window.

-  Fuzzy Matches pane: Dropped ``.tmx`` files will be copied to the
   ``tm`` folder.

-  Glossary pane: Dropped files with known glossary extensions
   (``.txt``, ``.tab``, etc.) will be copied to the ``glossary`` folder.

Editor
======

This is where you type and edit your translation. The Editor pane
displays the text of the partially translated document: the text already
translated is displayed in translation while the untranslated text is
displayed in the original language. The displayed text is split into
segments and you may scroll through the document and double-click on any
segment to open and edit it. In the above case, the segments already
translated are shown in yellow.

One of the above segments is the current segment. It is the segment that
is displayed in two parts. The upper part is in the source language, in
bold characters with a green background color, the lower part is the
editing field, ended by a marker: the marker is ``<segment nnnn>`` where
nnnn is a number of the segment in the project. Use the upper part as a
reference and replace or modify the contents of the editing field with
your translation.

.. note::
  the segment marker displays ``<segment nnnn +yy more> when the segment is non-unique. In that case, yy is the number of other occurrences of the segment in the project.``

Depending upon the preferred editing behavior, the editing field for the
untranslated segment may be empty, contain the source text, or contain
the translation of the string most similar to the one to be translated.
When you move to another segment, the translation is validated and
stored. If you want the translation to be the same as the source, simply
make the editing field empty by removing all the text (select all with
Ctrl+A and delete with Del). OmegaT is able to store translations that
are identical to the source. This is useful for documents that contain
trade marks, names or other proper nouns, or parts in a third language
that do not require translation. See *Translation editing* for more
details.

If you right click on the Editor pane, a pop-up menu opens,
offering\ **Cut, Copy, Paste** (i.e. same functions as +Ctrl+ +X+ ,
+Ctrl+ +C+ and +Ctrl+ +V+ ), **GoTo segment** and **Add glossary entry**
functions. In addition, when the right click occurs on an opened
segment, other options concerning **Alternative translations** are
proposed, for example to to jump to another instance of non-unique
segments.

It is possible to drag text from anywhere in the main window and to drop
it within the segment. Texted dragged from outside the target segment is
copied, while text dragged from within the segment is moved.

By default, it is not possible to select words in the source segment
using the keyboard rather than the mouse. Pressing F2 key allows to move
the cursor into the source segment (or anywhere in the editor) with the
keyboard arrows. In this mode, "Cursor lock off" is displayed at the
bottom of the pane. To come back to the standard mode "Cursor lock on",
press F2 again.

Fuzzy Matches
=============

The match viewer shows the most similar segments from translation
memories, both from internal project translation memory created in real
time as you translate your project and from ancillary translation
memories you have imported from your earlier jobs, or received from your
client or translation agency.

When you move to the next segment, the first fuzzy match (the one with
the best matching percentage) is automatically selected. You may select
a different match by pressing Ctrl+2, 3, 4, or 5. Of course, pressing
+Ctrl+ +5+ will have no effect, if there is no match #5. To use the
selected match in your translation, use Ctrl+R to replace the target
field with the match or use Ctrl+I to insert it at the cursor position.

The matching percentage is roughly equivalent to taking the number of
common words in the matched and the matching segment and dividing by the
number of words in the longer of the two. The selected fuzzy match is
highlighted in bold, words that are missing in the segment you are
translating are colored blue and words adjacent to the missing parts
green. In the above example the source segment is **Context menu
command**. The top match is 100%, because all words match. So do the
next two matches, and the match #4 is similar, but different. The line
with the matching percentage also includes the name of the translation
memory containing the match. If there's no file name displayed, the
source is the internal project translation memory. Orphan segments (the
match #2) describe segments in the default project translation memory
that have no corresponding source segment.

Glossary
========

The Glossary pane allows you to access your own collection of
expressions and specialist terminology which you have built up in your
glossary files. It shows translation of terms found in the current
segment. The source segment in the example below was “\ *Context menu
command*\ ”, as in the Fuzzy Matches example above, and the terms shown
were found in the glossaries, available (Microsoft's Term collection and
Slovenian Linux User group Glossary).

If you have TransTips option activated (Options → TransTips), you can
right click on the highlighted word in the source segment to open a
pop-up menu with suggested translation, as offered by your glossary.
Selecting one of them will insert it at the current cursor position into
the target segment. You can also highlight your preferred alternative in
the glossary pane and insert it into the target by right clicking on the
selection.

Dictionary
==========

Dictionaries are the electronic equivalents of printed dictionaries like
Merriam Webster, Duden, Larousse etc., that you may have on your desk.
See more about them in the chapter on
`Dictionaries <#appendix.dictionaries>`__

Machine Translation
===================

The machine translation pane, when opened, contains the suggestions by
machine translation tools for the current segment. Press Ctrl+M to
replace the translation of the current segment with the suggested
translation.

Multiple Translations
=====================

A given source segment may require several different translations,
depending on the context. If the current translation of the segment does
not fit, the user can select Edit → Create Alternative Translation. The
target text entered after that will be treated as an alternative
translation of the source segment. You can define one of the alternative
- for instance the most probable among them - as default translation by
selecting Edit → Use as Default Translation

Notes
=====

The translator can add notes to the opened segment, for instance to come
back later to the segment and redo the translation, check that
alternative translations are correct or to ask colleagues for their
opinion. You can browse through notes using GoTo → Next Note and GoTo →
Previous Note.

Comments
========

Some of the file formats, specialized for translation work, for instance
PO, allow the inclusion of comments. This way the translator can be
provided the context about the segment to be translated. In the example
below, the author of the PO file included a warning for the translator
to check the length of the translation:

Status bar
==========

The status bar displays work-flow related messages at the bottom of the
main window. This bar gives the user feedback on specific operations
that are in progress. It also displays the number of fuzzy and glossary
matches for the current segment.

The counters in the lower right corner keep track of the progress of the
translation (numbers in the left hand column refer to the figure above):

+--------------+------------------------------------------------------------------+
| 27/27        | number of segments - translated vs total for the current file    |
+--------------+------------------------------------------------------------------+
| 9319/16338   | number of unique segments - translated vs total in the project   |
+--------------+------------------------------------------------------------------+
| 31175        | total number of segments (including repeats) in the project      |
+--------------+------------------------------------------------------------------+
| 103/114      | number of source and target characters in the current segment    |
+--------------+------------------------------------------------------------------+

Table: Main Window - counters

From a practical point of view, the most important pair of numbers is
the second pair: it tells, how much you have done so far, in relation to
the total or second number. The project in the example is evidently
finished, as all the unique segments have been translated.

.. |image0| image:: images/Minimize.png
   :width: 60.0%
.. |image1| image:: images/Maximize.png
   :width: 60.0%
.. |image2| image:: images/Restore.png
   :width: 60.0%
.. |image3| image:: images/Undock.png
   :width: 60.0%
.. |image4| image:: images/Dock.png
   :width: 60.0%
