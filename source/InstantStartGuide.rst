Learn to use OmegaT in 5 minutes!
=================================

Set up a new project Project Create / open new
==============================================

Note: On an Apple Mac, use the Command key instead of the Control key.

Menu Project
New...
To start using OmegaT, first create a project that will hold all your
files, such as your source file, translation memories, glossaries, and
eventually your translated file. In the Project menu, select New... and
type a name for your project. Remember where you are creating the
project, because you will need to return to it later.

After you give your project a name, the Create New Project dialog will
open. At the top of that dialog, select your source file's language and
the language that your translated file will be, and click OK to
continue.

If you are interested in other settings of this dialog, you can return
to it any time by pressing Ctrl+E.

Next, the Project Files dialog opens. Click on Copy Files to Source
Folder... to select your source files. OmegaT will then copy the
selected files to the ``/source/`` subfolder of your newly created
project. After the source files have loaded in the Editor pane, you can
close the Project Files dialog.

Translate the file
==================

OmegaT will present one segment at a time for you to translate. After
you have translated each segment, press Ctrl+U to move to the next
untranslated segment (or Ctrl+Shift+U to move to the next translated
segment). Whenever you want to see what your translation will look like
in its final format, press Ctrl+D to generate the translated documents,
which will be created in the ``/target/`` subfolder of your project
folder. During translation, use the Edit and Go To menus to perform
various useful functions.

Validate your tags
==================

If your source files are formatted files, e.g. Microsoft Word,
LibreOffice Writer or HTML, OmegaT will convert the formatting into tags
that surround the text that you translate. Often documents will also
have tags that have nothing to do with formatting, but which are also
important in the source files (and in the translated files). A source
sentence might look like:

OmegaT, however, will present this sentence in the following fashion:

The tags in OmegaT are greyed, so they are easy to recognise. They are
protected, so that you cannot modify their contents, but you can delete
them, enter them by hand or move them around in the target sentence.
However, if you made mistakes when you typed the formatting tags, your
translated files might fail to open. Therefore, press Ctrl+Shift+V
before you generate your translated files, to validate that your tags
are correct.

Generate the translated file
============================

Once you have made certain that there are no tag errors in your
translation, press Ctrl+D to generate the target files, which will be
created in the ``/target/`` subfolder of your project folder.

Few more things to remember
===========================

-  If a file does not load into the Editor pane, then it could be that
   it is in a format that doesn't work in OmegaT. See Options >
   Preferences... > File Filters for a list of file formats that OmegaT
   can handle.

-  You can create a new project for each new job, and you can add new
   source files to a project at anytime.

-  To remind yourself of the project's initial settings, open the
   project properties dialog by pressing Ctrl+E. To see a list of files
   in the project, open the Project Files dialog by pressing Ctrl+L.

-  At the end of your translation, OmegaT exports three translation
   memories called ``level1``, ``level2`` and ``omegat`` to your project
   folder. The ``level1`` and ``level2`` memories can be shared with
   users of other translation programs. The memory named ``omegat`` can
   be used by OmegaT itself, in future projects that you create. If you
   place such translation memory files in the ``/tm/`` subfolder of a
   project, OmegaT will automatically search them for similar segments,
   called "fuzzy matches".

-  You can add a new term to the glossary by pressing Ctrl+Shift+G, or
   copy existing glossaries to the ``/glossary/`` subfolder of your
   project folder, and OmegaT will automatically look up words in them.

-  It is often useful to search for words and phrases in the source text
   and in your translation, so press Ctrl+F for the Text Search dialog
   at any time.

-  For a more comprehensive introduction see `OmegaT for
   beginners <https://omegat.org/files/OmegaT_for_Beginners.pdf>`__ on
   the OmegaT web site. If you need assistance with any aspect of
   OmegaT, feel free to join the `OmegaT users
   group. <https://groups.yahoo.com/neo/groups/OmegaT/info>`__
