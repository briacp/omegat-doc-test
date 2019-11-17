Project Properties
==================

This dialog is accessible by selecting Project > Properties...

Languages
---------

You can either enter the source and target languages by hand or use the
drop down menus. Bear in mind that changing the languages may render the
currently used translation memories useless since their language pair
may not longer match the new languages.

Tokenizers corresponding to the selected languages are displayed.

Options
-------

Enable Sentence-level segmentation
    The segmentation settings only address the way the source files are
    handled by OmegaT. The predominant way of segmenting the sources is
    the sentence-level segmenting, so this check box should in a normal
    case be left checked.

    In some seldom cases the alternative, i.e. segmenting by paragraphs,
    may be preferred. Changing this flag does not modify the
    segmentation of already existing translation memories. If you decide
    mid-translation to switch from sentence to paragraph translation,
    the internal translation memory of the project will not be changed
    (OmegaT may upgrade old translation memories that did not use
    sentence segmentation, but not vice versa), but OmegaT will attempt
    to create paragraph fuzzy matches by gluing together existing
    sentence translations.

    Changing segmentation settings may cause some already translated
    segments to be split or merged. This will effectively return them to
    the "untranslated" status, as they will no longer match segments
    recorded in the project memory, even though their original
    translation is still there.

Auto-propagation of Translations
    In case there are non-unique segments in source documents, the
    Auto-propagation check box offers the user the following two
    possibilities as regards automatic translation: if checked, the
    first translated segment will be assumed as the default translation
    and its target text will be automatically used for later hits during
    the translation process. Mistranslated segments can of course be
    corrected later manually using Create Alternative Translation. If
    the Auto-propagation check box is not checked, the segments with
    alternative translations are left untranslated until the user has
    decided which translation is to be used.

Remove Tags
    When enabled, all the formatting tags are removed from source
    segments. This is especially useful when dealing with texts where
    inline formatting is not really useful (e.g., OCRed PDF, bad
    converted .odt or .docx, etc.) In a normal case it should always be
    possible to open the target documents, as only inline tags are
    removed. Non-visible formatting (i.e., which doesn't appear as tags
    in the OmegaT editor) is retained in target documents.

External Post-processing Command
    This area allows entering an external post-processing command (for
    instance, a script to rename files) that will be applied each time
    Create Translated Documents is used. This external command cannot
    include "pipes", etc., which is why calling a script is recommended.

Segmentation...
    The segmentation rules are generally valid across all the projects.
    The user, however, may need to generate a set of rules, specific to
    the project in question. Use this button to open a dialog, activate
    the check box Project specific segmentation rules, then proceed to
    adjust the segmentation rules as desired. The new set of rules will
    be stored together with the project and will not interfere with the
    general set of segmentation rules. To delete project specific
    segmentation rules, uncheck the check box. See `Segmentation Setup
    preferences <#dialogs.preferences.segmentationsetup>`__ for more
    information on segmentation rules.

    *Hint:* the set of segmentation rules for a given project is stored
    as ``project/omegat/segmentation.conf.``

File Filters...
    In a similar fashion as above the user can create project-specific
    File filters, which will be stored together with the project and
    will be valid for the current project only. To create a
    project-specific set of file filters, click on the File filter
    ...button, then activate Enable project specific filters check box
    in the window that opens. A copy of the changed filters
    configuration will be stored with the project. To delete project
    specific file filters, uncheck the check box. Note that in the menu
    Options->File Filters, the global user filters are changed, not the
    project filters. See `File Filters
    preferences <#dialogs.preferences.filefilters>`__ for more on the
    subject.

    *Hint:* the set of file filters for a given project is stored as
    ``project/omegat/filters.xml.``

Repository Mapping...
    When working on a team project, this window allows you to define the
    mapping between remote folders and local folders (see examples
    `here <#howto.setupteamproject.mappingparameters>`__).

External Search...
    Defines the project-specific external search resources.

File locations
--------------

Here you can select different subfolders, for instance the subfolder
with source files, subfolder for target files etc. If you enter names of
folders that do not exist yet, OmegaT creates them for you. In case you
decide to modify project folders, keep in mind that this will not move
existing files from old folders to the new location.

Clic on Exclusions... to define the files or folders that will be
ignored by OmegaT. An ignored file or folder:

-  is not displayed in the Editor pane,

-  is not taken into account in statistics,

-  is not copied in /target folder during the translated files creation
   process.

In the Exclusion patterns dialog, it is possible to Add or Remove a
pattern, or edit one by selecting a line and pressing F2. It is possible
to use wildcards, using the `ant
syntax <https://ant.apache.org/manual/dirtasks.html#patterns>`__.
