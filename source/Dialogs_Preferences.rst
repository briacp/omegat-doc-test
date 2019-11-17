General Preferences
===================

This dialog is accessible by selecting Options > Preferences...

It allows parameters to be set for all translation projects.

General
-------

Use TAB to Advance
    Sets the segment validation key to Tab instead of the default Enter.
    This option is useful for some Chinese, Japanese or Korean character
    input systems.

Always Confirm Quit
    The program will seek confirmation before closing down.

Machine Translation
-------------------

Automatically fetch translations
    For confidentiality reasons, you may want to not send all the
    segments to the Machine Translation engine. If you uncheck this
    option, machine translations will be fetched only when you press
    +Ctrl+ +M+ ( +Cmd+ +M+ on OS X) in the current segment. You must
    then press +Ctrl+ +M+ again to insert the suggestion.

Untranslated segments only
    Check this box to send only untranslated segments to the machine
    translation services.

Select a supplier from the list and, if necessary, click Configure to
enter the identification details provided by the supplier.

The procedures for configuring access to the Microsoft Translator and
Google Translate services are described
`here <https://sourceforge.net/p/omegat/wiki/Configuring Machine Translation Services>`__.

Glossary
--------

Display context description for TBX glossaries
    Uncheck this option if the context description shown for each
    glossary entry is unnecessary or too long.

Use terms appearing separately in the source text
    When this option is checked, the glossary will display pairs or
    groups of words (expressions) even if the words within them appear
    separately in the source text.

    Uncheck this option if the glossary displays too many false
    positives.

Use stemming for glossary entries
    Select this option if you want the glossary to display words that
    have the same root.

Replace glossary hits when inserting source text
    If both this option and the `Insert the source
    text <#dialogs.preferences.editor.insertthesourcetext>`__ option are
    selected, all words with a corresponding glossary entry will be
    translated automatically when the source text is inserted.

Ignore hits with very different case (e.g. FOO vs foo)
    If this option is checked, the glossary will only display one entry,
    even if the same word exists in several forms (e.g. with and without
    capital letters) in the glossary.

TaaS Terminology
~~~~~~~~~~~~~~~~

Get API Key
    Click this button to access the
    `TaaS <https://term.tilde.com/taas>`__ project site and create a
    user account.

    You can then create an access key on the page
    https://term.tilde.com/account/keys/create?system=omegaT.

Store for this session only
    If this option is selected, OmegaT will not remember the access key
    between sessions.

Browse TaaS Collections...
    This button enables you to browse and download the collections that
    exist for the project's source and target languages. Private
    collections are displayed in bold. The collections are downloaded as
    TBX glossaries and stored in the current glossary folder.

Select TaaS Terminology Lookup Domain...
    If necessary, you can select a specific domain to limit the volume
    of data sent and received.

Dictionary
----------

Automatically search segment text in dictionary
    Clear this option to deactivate automatic searching – if
    dictionaries are too long, for example.

Use fuzzy matching for dictionary entries
    Select this option if you want dictionaries to display words that
    have the same root.

Appearance
----------

Restore Main Window
    Restores the components of the main OmegaT window to their default
    state. Use this feature when you have undocked, moved or hidden one
    or more components and you are unable to restore the desired
    arrangement. It can also be used when panes do not appear as
    expected following an OmegaT upgrade.

Font
~~~~

Shows the dialog to modify the text display font. Users of old computers
who feel window resizing is very slow can try changing the font. See
font settings in Miscellanea

Colours
~~~~~~~

This page allows you to choose different colours for each part of the
user interface.

Pre-defined themes can be set using scripts. A script bundled with
OmegaT called Switch Colour Themes provides a default "Dark" theme.

File Filters
------------

This dialog lists the file filters available. The filters used by the
current project are displayed in bold. If you prefer not to use OmegaT
to translate files of a certain type, you can turn off the corresponding
filter by deactivating the check box beside its name. OmegaT will then
omit the corresponding files when loading projects, and will copy them
unmodified to the target folder when creating target documents. When you
wish to use the filter again, just tick the check box. Click
**Defaults** to reset the file filters to the default settings. To edit
the files and encodings a filter is used for, select the filter in the
list and click **Edit.**

The dialog allows you to enable or disable the following options:

-  Remove leading and trailing tags: uncheck this option to display all
   the tags, including tags at the beginning and end of the segment.
   Warning: in Microsoft Open XML formats (docx, xlsx, etc.), if all
   tags are displayed, DO NOT place any text before the first tag – it
   is a technical tag that must always begin the segment.

-  Remove leading and trailing whitespace in non-segmented projects: by
   default, OmegaT removes leading and trailing whitespace. In
   non-segmented projects, it is possible to keep it by unchecking this
   option.

-  Preserve spaces for all tags: check this option if the source
   documents contain significant spaces used to control the layout that
   must not be ignored.

-  Ignore file context when identifying segments with alternate
   translations: by default, OmegaT uses the source file name as part of
   the identification of an alternative translation. If the option is
   checked, the source file name will not be used, and alternative
   translations will take effect in any file as long as the other
   context (previous/next segments or some sort of segment identifier,
   depending on the file format) matches.

Filter options
~~~~~~~~~~~~~~

Several filters (text files, XHTML files, HTML and XHTML files,
OpenDocument files and Microsoft Open XML files) have one or more
specific options. To modify the options, select the filter in the list
and click **Options**. The available options are:

**Text files**

-  *Paragraph segmentation on line breaks, empty lines or never:*

   if sentence segmentation rules are active, the text will be segmented
   further according to the option selected here.

**PO files**

-  *Allow blank translations in the target file*:

   If selected, when a segment in a PO file (which may be a whole
   paragraph) is not translated, the translation will be empty in the
   target file. Technically speaking, the ``msgstr`` segment in the PO
   target file, if created, will be left empty. As this is the standard
   behaviour for PO files, it is selected by default. If the option is
   off, the source text will be copied to the target segment.

-  *Skip PO header*

   The PO header will be skipped and left unchanged if this option is
   checked.

-  *Auto replace 'nplurals=INTEGER; plural=EXPRESSION;' in header*

   *This option allows OmegaT to override the specification in the PO
   file header and use the default for the selected target language.*

**XHTML Files**

-  *Translate the following attributes*: the selected attributes will
   appear as segments in the Editor window.

-  *Start a new paragraph on*: the <br> HTML tag will constitute a
   paragraph break for segmentation purposes.

-  *Skip text matching regular expression*: any text matching the
   regular expression is skipped. It is shown in red in the tag
   validator. Text in source segments that matches is shown in italics.

-  *Do not translate the content attribute of meta-tags ...:* The
   meta-tags in the box will not be translated.

-  *Do not translate the content of tags with the following attribute
   key-value pairs (separate with commas)*: if a tag matches the list of
   key-value pairs, its content will be ignored.

   It is sometimes useful to be able make certain tags untranslatable
   based on the values of their attributes. For example,
   ``<div class="hide"> <span translate="no">``. You can define
   key-value pairs for tags to be left untranslated. For the example
   above, the field would contain: ``class=hide, translate=no ``.

**Microsoft Office Open XML files**

You can select which elements are to be translated. They will appear as
separate segments in the translation.

-  **Word:** non-visible instruction text, comments, footnotes,
   endnotes, footers

-  **Excel:**\ comments, sheet names

-  **Power Point**: slide comments, slide masters, slide layouts

-  **Global:** charts, diagrams, drawings, WordArt

-  **Other Options:**

   -  *Aggregate tags*: if checked, tags with no translatable text
      between them will be aggregated into a single tag.

   -  *Preserve spaces for all tags*: if checked, "white space" (i.e.
      spaces and newlines) will be preserved, even if this option is not
      defined in the document.

**HTML and XHTML files**

-  *Add or rewrite encoding declaration in HTML and XHTML files*: the
   target files often need to have a different character set encoding
   from the one in the source file (whether it is explicitly defined or
   implied). Using this option, the translator can specify whether the
   target files should have the encoding declaration included. For
   instance, if the file filter specifies UTF8 as the encoding scheme
   for the target files, selecting Always will ensure that this
   information is included in the translated files.

-  *Translate the following attributes*: the selected attributes will
   appear as segments in the Editor window.

-  *Start a new paragraph on*: the <br> HTML tag will constitute a
   paragraph break for segmentation purposes.

-  *Skip text matching regular expression*: any text matching the
   regular expression is skipped. It is shown in red in the tag
   validator. Text in source segments that matches is shown in italics.

-  *Do not translate the content attribute of meta-tags ...:* The
   meta-tags in the box will not be translated.

-  *Do not translate the content of tags with the following attribute
   key-value pairs (separate with commas)*: if a tag matches the list of
   key-value pairs, its content will be ignored.

   It is sometimes useful to be able make certain tags untranslatable
   based on the values of their attributes. For example,
   ``<div class="hide"> <span translate="no">``. You can define
   key-value pairs for tags to be left untranslated. For the example
   above, the field would contain: ``class=hide, translate=no ``.

-  *Compress whitespace in translated document*: multiple continuous
   whitespace characters will be converted into one single whitespace in
   the translated document.

-  *Remove HTML comments in translated document*: commented parts
   (between <!-- and -->) will not be copied into the translated
   document.

**Open Document Format (ODF) files**

-  You can select which of the following items are to be translated:

   index entries, bookmarks, bookmark references, notes, comments,
   presentation notes, links (URL), sheet names

Edit filter dialog
~~~~~~~~~~~~~~~~~~

This dialog enables you to specify the source filename patterns for
files to be processed by the filter, customize the filenames of
translated files and select which encodings should be used for loading
the source file and saving the translation. To modify a file filter
pattern, either modify the fields directly or click **Edit**. To add a
new file filter pattern, click **Add**. The same dialog is used to add a
pattern or to edit a particular pattern. The dialog includes a special
target filename pattern editor, which you can use to customize the names
of output files.

Source file type, filename pattern
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

When OmegaT encounters a file in its source folder, it attempts to
select the filter based upon the file's extension. More precisely,
OmegaT attempts to match each filter's source filename patterns against
the filename. For example, the pattern ``*.xhtml ``\ matches any file
with the ``.xhtml`` extension. If the appropriate filter is found, the
file is assigned to it for processing. For example, by default, the
XHTML filter is used to process files with the .xhtml extension. You can
change or add filename patterns for files to be handled by each file
filter. Source filename patterns use wild card characters similar to
those used in **Searches.**\ The '\*' character matches zero or more
characters. The '?' character matches exactly one character. All other
characters represent themselves. For example, if you wish the text
filter to handle readme files (``readme, read.me``, and ``readme.txt``)
you should use the pattern ``read*``.

Source and Translated file encoding
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Only a limited number of file formats specify a mandatory encoding. File
formats that do not specify their encoding will use the encoding you set
up for the extension that matches their name. For example, by default
``.txt`` files will be loaded using the default encoding of your
operating system. You can change the source encoding for each different
source filename pattern. Target files can also be written in any
encoding. By default, the translated file encoding is the same as the
source file encoding. The source and target encoding fields use
drop-down menus containing all the supported encodings. <auto> leaves
the choice of encoding to OmegaT. This is how it works:

-  OmegaT identifies the source file encoding by using its encoding
   declaration, if present (HTML files, XML based files).

-  OmegaT is instructed to use a mandatory encoding for certain file
   formats (Java properties etc).

-  OmegaT uses the default encoding of the operating system for text
   files.

Translated filename
^^^^^^^^^^^^^^^^^^^

Sometimes you may wish to rename the files you translate automatically,
for example adding a language code after the file name. The target
filename pattern uses a special syntax, so if you want to edit this
field, you must click **Edit...**\ and use the Edit Pattern Dialog. If
you want to revert to the filter's default configuration, click
**Defaults.** You can also modify the name directly in the target
filename pattern field of the file filters dialog. The Edit Pattern
Dialog offers among others the following options:

-  Default is ``${filename}``– full filename of the source file with
   extension: in this case the name of the translated file is the same
   as that of the source file.

-  ``${nameOnly}``– allows you to insert only the name of the source
   file without the extension.

-  ``${extension} ``- the original file extension

-  ``${targetLocale}``– target locale code (of a form "xx\_YY").

-  ``${targetLanguage}``– the target language and country code together
   (of a form "XX-YY").

-  ``${targetLanguageCode}`` – the target language - only "XX"

-  ``${targetCountryCode}``– the target country - only "YY"

-  ``${timestamp-????}`` – system date time at generation time in
   various patterns

   See `Oracle
   documentation <http://docs.oracle.com/javase/1.4.2/docs/api/java/text/SimpleDateFormat.html>`__
   for examples of the "SimpleDateFormat" patterns

-  ``${system-os-name}`` - operating system of the computer used

-  ``${system-user-name}`` - system user name

-  ``${system-host-name}`` - system host name

-  ``${file-source-encoding}`` - source file encoding

-  ``${file-target-encoding}`` - target file encoding

-  ``${targetLocaleLCID}`` - Microsoft target locale

Additional variants are available for variables ${nameOnly} and
${Extension}. In case the file name has ambivalent name, one can apply
variables of the form ``${name
        only``\ *-extension number*} and ``${extension``-*extension
number}*. If for example the original file is named Document.xx.docx,
the following variables will give the following results:

-  ``${nameOnly-0}`` Document

-  ``${nameOnly-1}`` Document.xx

-  ``${nameOnly-2}`` Document.xx.docx

-  ``${extension-0}`` docx

-  ``${extension-1}`` xx.docx

-  ``${extension-2}`` Document.xx.docx

Segmentation Setup
------------------

Translation memory tools work with textual units called segments. OmegaT
has two ways to segment a text: by paragraph or by sentence segmentation
(also referred to as “rule-based segmentation”). In order to select the
type of segmentation, select Project > Properties... from the main menu
and tick or untick the check box provided. Paragraph segmentation is
advantageous in certain cases, such as highly creative or stylistic
translations in which the translator may wish to change the order of
entire sentences; for the majority of projects, however, sentence
segmentation is a choice to be preferred, since it delivers better
matches from previous translations. If sentence segmentation has been
selected, you can setup the rules by selecting Options >
Segmentation...from the main menu.

Dependable segmentation rules are already available for many languages,
so it is likely that you will not need to get involved with writing your
own segmentation rules. On the other hand this functionality can be very
useful in special cases, where you can increase your productivity by
tuning the segmentation rules to the text to be translated.

**Warning:**\ because the text will segment differently after filter
options have been changed, so you may have to start translating from
scratch. At the same time the previous valid segments in the project
translation memory will turn into orphan segments. If you change
segmentation options when a project is open, you must reload the project
in order for the changes to take effect.

OmegaT uses the following sequence of steps:

Structure level segmentation
    OmegaT first parses the text for structure-level segmentation.
    During this process it is only the structure of the source file that
    is used to produce segments.

    For example, text files may be segmented on line breaks, empty
    lines, or not be segmented at all. Files containing formatting (ODF
    documents, HTML documents, etc.) are segmented on the block-level
    (paragraph) tags. Translatable object attributes in XHTML or HTML
    files can be extracted as separate segments.

Sentence level segmentation
    After segmenting the source file into structural units, OmegaT will
    segment these blocks further into sentences.

Segmentation rules
~~~~~~~~~~~~~~~~~~

The process of segmenting can be pictured as follows: the cursor moves
along the text, one character at a time. At each cursor position rules,
consisting of a **Before**\ and **After**\ pattern, are applied in their
given order to see if any of the\ **Before** patterns are valid for the
text on the left and the corresponding **After** pattern for the text on
the right of the cursor. If the rule matches, either the cursor moves on
without inserting a segment break (for an exception rule) or a new
segment break is created at the current cursor position (for the break
rule).

The two types of rules behave as follows:

Break rule
    Separates the source text into segments. For example, "*Did it make
    sense? I was not sure*." should be split into two segments. For this
    to happen, there should be a break rule for "?", when followed by
    spaces and a capitalized word. To define a rule as a break rule,
    tick the Break/Exception check box.

Exception rule
    specify what parts of text should NOT be separated. In spite of the
    period, *"Mrs. Dalloway "* should not be split in two segments, so
    an exception rule should be established for Mrs (and for Mr, for Dr,
    for prof etc), followed by a period. To define a rule as an
    exception rule, leave the Break/Exception check box unticked.

The predefined break rules should be sufficient for most European
languages and Japanese. In view of the flexibility, you may consider
defining more exception rules for your source language in order to
provide more meaningful and coherent segments.

Rule priority
~~~~~~~~~~~~~

All segmentation rule sets for a matching language pattern are active
and are applied in the given order of priority, so rules for specific
language should be higher than default ones. For example, rules for
Canadian French (FR-CA) should be set higher than rules for French
(FR.\*), and higher than Default (.\*) ones. Thus, when translating from
Canadian French the rules for Canadian French - if any - will be applied
first, followed by the rules for French and lastly, by the Default
rules.

Creating a new rule
~~~~~~~~~~~~~~~~~~~

Major changes to the segmentation rules should be generally avoided,
especially after completion of the first draft, but minor changes, such
as the addition of a recognized abbreviation, can be advantageous.

In order to edit or expand an existing set of rules, simply click on it
in the top table. The rules for that set will appear in the bottom half
of the window.

In order to create an empty set of rules for a new language pattern
click **Add**\ in the upper half of the dialog. An empty line will
appear at the bottom of the upper table (you may have to scroll down to
see it). Change the name of the rule set and the language pattern to the
language concerned and its code. The syntax of the language pattern
conforms to regular expression syntax. If your set of rules handles a
language-country pair, we advise you to move it to the top using the
**Move Up** button.

Add the **Before** and\ **After** patterns. To check their syntax and
their applicability, it is advisable to use tools which allow you to see
their effect directly. See `Regular expressions <#appendix.regexp>`__. A
good starting point will always be the existing rules.

A few simple examples
~~~~~~~~~~~~~~~~~~~~~

+---------------------------------------------------------------------------+--------------+---------+------------------------------------------------------------------------------------------------------------+
| Intention                                                                 | Before       | After   | Note                                                                                                       |
+===========================================================================+==============+=========+============================================================================================================+
| Set the segment start after a period ('.') followed by a space, tab ...   | \\.          | \\s     | "\\." stands for the period character. "\\s" means any white space character (space, tab, new page etc.)   |
+---------------------------------------------------------------------------+--------------+---------+------------------------------------------------------------------------------------------------------------+
| Do not segment after Mr.                                                  | Mr\\.        | \\s     | This an exception rule, so the rule check box must not be ticked                                           |
+---------------------------------------------------------------------------+--------------+---------+------------------------------------------------------------------------------------------------------------+
| Set a segment after "。" (Japanese period)                                | 。           |         | Note that ``after`` is empty                                                                               |
+---------------------------------------------------------------------------+--------------+---------+------------------------------------------------------------------------------------------------------------+
| Do not segment after M. Mr. Mrs. and Ms.                                  | Mr??s??\\.   | \\s     | Exception rule - see the use of ? in regular expressions                                                   |
+---------------------------------------------------------------------------+--------------+---------+------------------------------------------------------------------------------------------------------------+

Auto-Completion
---------------

Click on Glossary... to configure the Auto-completer Glossary View.

Click on Auto-text... to configure Auto-text options and to add or
remove entries.

Click on Character Table... to set the Character table auto-completer
options.

Auto-completer is launched within the target segment via **Ctrl+Space**
shortcut.

If **Show Relevant Suggestions Automatically** option is checked,
Auto-completer is launched automatically by typing the first letter of a
translated glossary entry, or by typing "<" in case of tags.

Spellchecker
------------

OmegaT has a built-in spell checker based on the `spelling
checker <#appendix.spellchecker>`__ used in Apache OpenOffice,
LibreOffice, Firefox and Thunderbird. It is consequently able to use the
huge range of free spelling dictionaries available for these
applications.

LanguageTool plug-in
--------------------

Service type
    Select the location of the language checker.

    Using a different language checker on your local machine than the
    one supplied with OmegaT gives you the option of personalising the
    verification rules.

Rules
    Check or uncheck the rules depending on whether they are relevant to
    the type of text you are translating.

External Search
---------------

Enable project-specific commands
    By default, OmegaT does not execute the commands specified in the
    project-specific settings (the ``finder.xml`` file in the ``omegat``
    folder), because they may have a critical impact on the machine's
    security.

    Only activate this option if you know what you are doing, and only
    for projects from trusted sources.

Context Menu Priority:
    Enables you to change the order of the commands in the context menu
    (the right-click menu). Values around 100 display commands at the
    top, and values around 900 display them at the bottom.

    You will need to restart OmegaT for this change to take effect.

Editor
------

Insert the source text
    You can have the source text inserted automatically into the editing
    field. This is useful for texts containing many trade marks or other
    proper nouns you which must be left unchanged.

Leave the segment empty
    OmegaT leaves the editing field blank. This option allows you to
    enter the translation without the need to remove the source text,
    thus saving you two keystrokes (**Ctrl+A**\ and **Del).** Empty
    translations are now allowed. They are displayed as <EMPTY> in the
    Editor. To create one, right-click in a segment, and select "**Set
    empty translation**". The entry **Remove translation** in the same
    pop up menu also allows to delete the existing translation of the
    current segment. You achieve the same by clearing the target segment
    and pressing Enter.

Insert the best fuzzy match
    OmegaT inserts the translation of the string most similar to the
    current source, if it is above the similarity threshold that you
    have selected in this dialog. The prefix (per default empty) can be
    used to tag translations, done via fuzzy matches. If you add a
    prefix (for instance [fuzzy]), you can trace those translations
    later to see they are correct.

The check boxes in the lower half of the dialog window serve the
following purpose:

Attempt to convert numbers when inserting a fuzzy match
    If this option is checked, when a fuzzy match is inserted, either
    manually or automatically, OmegaT attempts to convert the numbers in
    the fuzzy matches according to the source contents. There are a
    number of restrictions:

    -  The source segment and the fuzzy matches must contain the same
       list of numbers

    -  The numbers must be exactly the same between the source and the
       target matches.

    -  Only integers and simple floats (using the period as a decimal
       character, e.g. 5.4, but not 5,4 or 54E-01) are considered.

Allow translation to be equal to source
    Documents for translation may contain trade marks, names or other
    proper nouns that will be the same in translated documents. There
    are two strategies for segments that contain only such invariable
    text.

    You can decide not to translate such segments at all. OmegaT will
    then report these segments as not translated. This is the default.
    The alternative is to enter a translation that is identical to the
    source text. OmegaT is able to recognize that you have done this. To
    make this possible, select this option.

Export the segment to text files
    The text export function exports data from within the current OmegaT
    project to plain text files. The data are exported when the segment
    is opened. The files appear in the /script subfolder in the OmegaT
    user files folder, and include:

    -  The content of the segment source text (``source.txt``).

    -  The content of the segment target text (``target.txt``).

    -  The text highlighted by the user, when Ctrl+Shift+C is pressed or
       Edit > Export Selection is selected (``selection.txt``).

    The content of the files is overwritten either when a new segment is
    opened (source.txt and target.txt) or when a new selection is
    exported (selection.txt). The files are unformatted plain text
    files. The whole process can be steered and controlled via
    Tck/Tcl-based scripting. See `Using the OmegaT text export
    function <http://www.omegat.org/en/howtos/text_export.html>`__ for
    specifics, examples and suggestions.

Go To Next Untranslated Segment stops where there is at least one
alternative translation
    If we want to avoid any mis-translations in case of segments with
    several possible target contents, checking this check box will cause
    **Go To Next Untranslated Segment** to stop on the next such
    segment, irrespective of whether it has already been translated or
    not.

Allow tag editing
    Uncheck this option to prevent any damage on the tags (i.e., partial
    deletion) during editing. Removing an entire tag remains possible in
    that case, by using Ctrl+Backspace/Delete or by selecting it
    completely (Ctrl+Shift+Left/Right) then deleting it (Delete or
    Ctrl+X).

Validate tags when leaving a segment
    Check this option to be warned about differences between source and
    target segments tags each time you leave a segment.

Save auto-populated status
    Check this option to record in the ``project_save.tmx`` file the
    information that a segment has been auto-populated, so it can be
    displayed with a specific color in the Editor (if the "Mark
    Auto-Populated Segments" option, in the View menu, is checked).

Initially load this many segments
    By default the editor displays 2,000 of initial segments, and
    progressively loads more as you scroll up or down. If you have a
    powerful machine, and/or if you don't like how the scrollbar behaves
    during progressive loading, you can increase this number.

Tag Processing
--------------

When translating software-related files, you can configure the Tag
Validator options to also check programming (%...) variables. You can
also define various options relating to tag validation and define custom
tags.

For example, if you enter ``\d+`` into the Regular expression for custom
tags field, all numbers will be considered as tags, enabling you to
check that numbers have not been changed by mistake during translation.

Similarly, enter ``<.*?>`` to make sure that HTML tags (for example)
entered into the source text are preserved without modification in the
translation.

Note: these two instructions can be combined by writing
``(<.*?>)|(\d+)``.

Team
----

Enter your name here and it will be attached to all segments translated
by you.

Repository Credentials
~~~~~~~~~~~~~~~~~~~~~~

List of projects for which login details are stored in OmegaT. Remove a
project from this list if you want OmegaT to ask you for a login and a
password every time you access the project.

TM Matches
----------

Sort fuzzy matches by:
    By default, the closest matches displayed in the Fuzzy Matches pane
    are determined using stemming.

    To obtain more literal matches closer to 100%, select the Full text,
    including tags and numbers option.

Displaying tags in non-OmegaT TMXs
    Decide how tags in foreign TMX files (i.e. not generated by OmegaT)
    are to be treated.

Match display template
    Change how fuzzy matches are displayed, through the use of
    pre-configured variables:

    +------------------------+----------------------------------------------------------------------------------------------------------------------------------------+
    | ``${id}``              | Number of the match from 1 to 5                                                                                                        |
    +------------------------+----------------------------------------------------------------------------------------------------------------------------------------+
    | ``${sourceText}``      | Source text of the match                                                                                                               |
    +------------------------+----------------------------------------------------------------------------------------------------------------------------------------+
    | ``${targetText}``      | Target text of the match                                                                                                               |
    +------------------------+----------------------------------------------------------------------------------------------------------------------------------------+
    | ``${diff}``            | String showing the differences between the source and the match.\ *Hint:* use this if the text you are translating has been updated.   |
    +------------------------+----------------------------------------------------------------------------------------------------------------------------------------+
    | ``${diffReversed}``    | Same as ${diff}, but with the differences (what is to be inserted and deleted) inverted.                                               |
    +------------------------+----------------------------------------------------------------------------------------------------------------------------------------+
    | ``${score}``           | Percentage calculated with Stemming, no tags and no numbers option.                                                                    |
    +------------------------+----------------------------------------------------------------------------------------------------------------------------------------+
    | ``${noStemScore}``     | Percentage calculated with No tags and no numbers option.                                                                              |
    +------------------------+----------------------------------------------------------------------------------------------------------------------------------------+
    | ``${adjustedScore}``   | Percentage calculated with Full text, including tags and numbers option.                                                               |
    +------------------------+----------------------------------------------------------------------------------------------------------------------------------------+
    | ``${fuzzyFlag}``       | Indicate that this match is fuzzy (currently only for translations from PO files with the #fuzzy mark)                                 |
    +------------------------+----------------------------------------------------------------------------------------------------------------------------------------+

    Table: Match pane setup

View
----

Contains options for displaying texts and modification information in
different ways.

Include the first non-unique segment when marking non-unique segments
    Check this option to display all non-unique segments (repetitions)
    in grey. When the option is unchecked, all non-unique segments are
    shown in grey except the first occurrence.

Saving and Output
-----------------

Allows the user select the interval - in minutes and seconds - between
consecutive automatic saves of the project.

Change the default interval (3 minutes) depending on the characteristics
of the project:

-  short intervals (minimum: 10 seconds) for synchronised projects on an
   internal server.

-  long intervals for team projects hosted on external servers.

External Post-processing Command
    Specify commands that are executed after the Create Translated
    Documents command.

    An example of the use of this feature would be to send translated
    documents automatically to the client's FTP server.

Also allow per-project external commands
    By default, OmegaT does not execute the commands specified in the
    project-specific settings (the ``omegat.project`` file), because
    they may have a critical impact on the machine's security.

    Only activate this option if you know what you are doing, and only
    for projects from trusted sources.

Proxy Login
-----------

If OmegaT needs to use an authenticated proxy server to access the
Internet, enter the details provided by the proxy administrator here.

Secure store
------------

Here you can redefine the master password used to protect login details
and access keys for machine translation services. Take care to make a
note of all these details before creating a new password, because they
will all be deleted and will need to be re-entered.

Plugins
-------

Gives access to the list of plugins available. Plugins are installed in
the ``/plugins`` folder.

Updates
-------

Enables automatic notification of OmegaT updates.
