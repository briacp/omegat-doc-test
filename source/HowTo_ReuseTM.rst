Reuse Translation Memories
==========================

Initially, that is when the project is created, the main TM of the
project, ``project_save.tmx`` is empty. This TM gradually becomes filled
during the translation. To speed up this process, existing translations
can be reused. If a given sentence has already been translated once, and
translated correctly, there is no need for it to be retranslated.
Translation memories may also contain reference translations:
multinational legislation, such as that of the European Community, is a
typical example.

When you create the target documents in an OmegaT project, the
translation memory of the project is output in the form of three files
in the root folder of your OmegaT project (see the above description).
You can regard these three tmx files (``-omegat.tmx``, ``-level1.tmx``
and ``-level2.tmx``) as an "export translation memory", i.e. as an
export of your current project's content in bilingual form.

Should you wish to reuse a translation memory from a previous project
(for example because the new project is similar to the previous project,
or uses terminology which might have been used before), you can use
these translation memories as "input translation memories", i.e. for
import into your new project. In this case, place the translation
memories you wish to use in the */tm* or */tm*/auto folder of your new
project: in the former case you will get hits from these translation
memories in the fuzzy matches viewer, and in the latter case these TMs
will be used to pre-translate your source text.

By default, the /tm folder is below the project's root folder (e.g.
...\ */MyProject/tm*), but you can choose a different folder in the
project properties dialog if you wish. This is useful if you frequently
use translation memories produced in the past, for example because they
are on the same subject or for the same customer. In this case, a useful
procedure would be:

-  Create a folder (a "repository folder") in a convenient location on
   your hard drive for the translation memories for a particular
   customer or subject.

-  Whenever you finish a project, copy one of the three "export"
   translation memory files from the root folder of the project to the
   repository folder.

-  When you begin a new project on the same subject or for the same
   customer, navigate to the repository folder in the Project >
   Properties > Edit Project dialog and select it as the translation
   memory folder.

Note that all the tmx files in the /tm repository are parsed when the
project is opened, so putting all different TMs you may have on hand
into this folder may unnecessarily slow OmegaT down. You may even
consider removing those that are not required any more, once you have
used their contents to fill up the ``project-save.tmx`` file.

Importing and exporting translation memories
--------------------------------------------

OmegaT supports imported tmx versions 1.1-1.4b (both level 1 and level
2). This enables the translation memories produced by other tools to be
read by OmegaT. However, OmegaT does not fully support imported level 2
tmx files (these store not only the translation, but also the
formatting). Level 2 tmx files will still be imported and their textual
content can be seen in OmegaT, but the quality of fuzzy matches will be
somewhat lower.

OmegaT follows very strict procedures when loading translation memory
(tmx) files. If an error is found in such a file, OmegaT will indicate
the position within the defective file at which the error is located.

Some tools are known to produce invalid tmx files under certain
conditions. If you wish to use such files as reference translations in
OmegaT, they must be repaired, or OmegaT will report an error and fail
to load them. Fixes are trivial operations and OmegaT assists
troubleshooting with the related error message. You can ask the user
group for advice if you have problems.

OmegaT exports version 1.4 TMX files (both level 1 and level 2). The
level 2 export is not fully compliant with the level 2 standard, but is
sufficiently close and will generate correct matches in other
translation memory tools supporting TMX Level 2. If you only need
textual information (and not formatting information), use the level 1
file that OmegaT has created.

Creating a translation memory for selected documents
----------------------------------------------------

In case translators need to share their TMX bases while excluding some
of their parts or including just translations of certain files, sharing
the complete ``ProjectName-omegat.tmx`` is out of question. The
following recipe is just one of the possibilities, but simple enough to
follow and without any dangers for the assets.

-  Create a project, separate for other projects, in the desired
   language pair, with an appropriate name - note that the TMXs created
   will include this name.

-  Copy the documents, you need the translation memory for, into the
   source folder of the project.

-  Copy the translation memories, containing the translations of the
   documents above, into ``tm/auto`` subfolder of the new project.

-  Start the project. Check for possible Tag errors with Ctrl+T and
   untranslated segments with Ctrl+U. To check everything is as
   expected, you may press Ctrl+D to create the target documents and
   check their contents.

-  When you exit the project. the TMX files in the main project folder
   (see above) now contain the translations in the selected language
   pair, for the files, you have copied into the source folder. Copy
   them to a safe place for future referrals.

-  To avoid reusing the project and thus possibly polluting future
   cases, delete the project folder or archive it away from your
   workplace.

Sharing translation memories
----------------------------

In cases where a team of translators is involved, translators will
prefer to share common translation memories rather than distribute their
local versions.

OmegaT interfaces to SVN and Git, two common team software versioning
and revision control systems (RCS), available under an open source
license. In case of OmegaT complete project folders - in other words the
translation memories involved as well as source folders, project
settings etc - are managed by the selected RCS. see more in Chapter

Using TMX with alternative language
-----------------------------------

There may be cases where you have done a project with e.g. Dutch
sources, and a translation in say English. Then you need a translation
in e.g. Chinese, but your translator does not understand Dutch; she,
however, understands perfectly English. In this case, the NL-EN
translation memory can serve as a go-between to help generate NL to ZH
translation.

The solution in our example is to copy the existing translation memory
into the tm/tmx2source/ subfolder and rename it to ZH\_CN.tmx to
indicate the target language of the tmx. The translator will be shown
English translations for source segments in Dutch and use them to create
the Chinese translation.

**Important:**\ the supporting TMX must be renamed XX\_YY.tmx, where
XX\_YY is the target language of the tmx, for instance to ZH\_CN.tmx in
the example above. The project and TMX source languages should of course
be identical - NL in our example. Note that only one TMX for a given
language pair is possible, so if several translation memories should be
involved, you will need to merge them all into the XX\_YY.tmx.
