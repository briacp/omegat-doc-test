Project folder
==============

An OmegaT project is a folder containing files and subfolders.

source
======

The source subfolder contains files to be translated. You can add the
files to it later. Note that the structure of the source subfolder may
take any form you like. If the files to be translated are parts of a
tree structure (as in a website), you need only specify the top-level
subfolder and OmegaT will maintain the entire contents, while keeping
the tree structure intact.

target
======

This subfolder is initially empty. To add contents to it, select Project
> Create Translated Documents. Files within the ``source`` folder,
whether translated or not, are then generated here, with the same
hierarchy as present in the source subfolder. The contents of the target
subfolder will reflect the current state of the translation, as present
in the project translation memory, saved in the current
**/omegat/project\_save.tmx**. Untranslated segments will hereby remain
in the source language.

tm
==

The /tm/ folder can contain any number of ancillary translation memories
- i.e. tmx files. Such files can be created in any of the three
varieties indicated above. Note that other CAT tools can export (and
import as well) tmx files, usually in all three forms. The best thing of
course is to use OmegaT-specific TMX files (see above), so that the
in-line formatting within the segment is retained.

The contents of translation memories in the tm subfolder serve to
generate suggestions for the text(s) to be translated. Any text, already
translated and stored in those files, will appear among the fuzzy
matches, if it is sufficiently similar to the text currently being
translated.

If the source segment in one of the ancillary TMs is identical to the
text being translated, OmegaT acts as defined in the Options > Editing
Behavior... dialog window. For instance (if the default is accepted),
the translation from the ancillary TM is accepted and prefixed
with\ *[fuzzy]*, so that the translator can review the translations at a
later stage and check whether the segments tagged this way, have been
translated correctly.

It may happen, that translation memories, available in the ``tm``
subfolder, contain segments with identical source text, but differing
targets. TMX files are read sorted by their names and segments within a
given TMX file line by line. The last segment with the identical source
text will thus prevail (Note: of course it makes more sense to avoid
this to happen in the first place).

Note that the TMX files in the tm folder can be compressed with gzip.

tm/auto
-------

If it is clear from the very start, that translations in a given TM (or
TMs) are all correct, one can put them into the\ **tm/auto** folder and
avoid confirming a lot of\ *[fuzzy]* cases.

1. Put the TMX in /tm/auto.

2. Open the project. The changes are displayed.

3. Make a slight change anywhere in the project. This modifies
   ``project_save.tmx`` (by adding proper Translation Units from "auto"
   TMX)

Note: if TMX is removed from /tm/auto before step 3, no extra
Translation Unit is added.

tm/enforce
----------

If you have no doubt that a TMX is more accurate than the
``project_save.tmx`` of OmegaT, put this TMX in /tm/enforce to overwrite
existing default translations unconditionally.

1. Put the TMX in /tm/enforce.

2. Open the project. The changes are displayed.

3. Make a slight change anywhere in the project. This modifies
   ``project_save.tmx``.

4. Make decision about immunity of the enforced segments:

   -  If they *don't need* to stay immune from further changes, then
      remove the TMX from /tm/enforce.

   -  If they *need* to stay immune from further changes, then keep the
      TMX in /tm/enforce.

Note: if TMX is removed from /tm/enforce before step 3, enforcements
aren't kept at all.

tm/mt
-----

In the editor pane, when a match is inserted from a TMX contained in a
folder named ``mt``, the background of the active segment is changed to
red. The background is restored to normal when the segment is left.

tm/penalty-xxx
--------------

Sometimes, it is useful to distinguish between high-quality translation
memories and those that are, because of the subject matter, client,
revision status, etc., less reliable. For translation memories in
folders with a name ``penalty-xxx`` (with xxx between 0 and 100),
matches will be degraded according to the name of the folder: a 100%
match in any of TMs, residing in a folder called ``penalty-30`` for
instance, will be lowered to a 70% match. The penalty applies to all
three match percentages: matches 75, 80, 90 will in this case be lowered
to 45, 50, 60.

dictionary
==========

Initially empty, this folder will contain dictionaries you have added to
the project. See `Dictionaries <#appendix.dictionaries>`__ for more on
this subject.

glossary
========

This folder is initially empty. It will contain glossaries you will be
using in the project. See `Glossaries <#appendix.glossaries>`__ for more
on this subject.

omegat
======

The **omegat** subfolder contains at least one and possibly several
other files. The most important file here is the
``project_save.tmx, ``\ that is the working translation memory for the
project. Backups of this file (with extension bak) are added
progressively to this subfolder, first at the beginning of the
translation session, at its end, and while the translation progresses.

During translation additional files may get created in this subfolder as
follows

stats.txt
    contains the current statistics of the current project. You can view
    it by selecting Tools > Statistics

ignored\_words.txt.; learned\_words.txt
    are created and used by the spell checker. If you already have
    collected words you wish the spell checker to ignore / accept, you
    just need to copy the corresponding two files into the
    ``omegat``\ subfolder of your current project.

project\_stats\_match.txt
    contains the latest project match statistics, generated by Tools >
    Match Statistics

segmentation.conf
    if existing, it contains project-specific segmentation rules.

filters.xml
    if existing, it contains project-specific file filters.

uiLayout.xml
    if existing, it contains project-specific GUI settings.

omegat.project (file)
=====================

Contains project parameters as defined in the `Project
properties <#dialogs.projectproperties>`__ dialog.

.repositories
=============

In a team project, this folder contains a versioned copy of the project
tree structure linked directly to the remote server.

You can make changes to remote files (e.g. deleting a file) using this
folder and a Git or SVN client.

In some operating systems, this folder is not displayed by default.
Activate the "Show hidden files" option to make it visible.
