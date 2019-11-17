Manage Right-To-Left languages
==============================

Justification of source and target segments depends upon the project
languages. By default, left justification is used for Left-To-Right
(LTR) languages and right justification for Right-To-Left (RTL)
languages. You can toggle between different display modes by pressing
+Shift+ +Ctrl+ +O+ (this is the letter O and not the numeral 0). The
+Shift+ +Ctrl+ +O+ toggle has three states:

-  default justification, that is as defined by the language

-  left justification

-  right justification

Using the RTL mode in OmegaT has no influence whatsoever on the display
mode of the translated documents created in OmegaT. The display mode of
the translated documents must be modified within the application (such
as Microsoft Word) commonly used to display or modify them (check the
relevant manuals for details). Using +Shift+ +Ctrl+ +O+ causes both text
input and display in OmegaT to change. It can be used separately for all
three panes (Editor, Fuzzy Matches and Glossary) by clicking on the pane
and toggling the display mode. It can also be used in all the input
fields found in OmegaT - in the search window, for segmentation rules
etc.

Mac OS X users, note: use +Shift+ +Ctrl+ +O+ shortcut and
**not**\ cmd+Ctrl+O.

Mixing RTL and LTR strings in segments
--------------------------------------

When writing purely RTL text, the default (LTR) view may be used. In
many cases, however, it is necessary to embed LTR text in RTL text. For
example, in OmegaT tags, product names that must be left in the LTR
source language, place holders in localization files, and numbers in
text. In cases like these it becomes necessary to switch to RTL mode, so
that the RTL (in fact bidirectional) text is displayed correctly. It
should be noted that when OmegaT is in RTL mode, both source and target
are displayed in RTL mode. This means that if the source language is LTR
and the target language is RTL, or vice versa, it may be necessary to
toggle back and forth between RTL and LTR modes to view the source and
enter the target easily in their respective modes.

OmegaT tags in RTL segments
---------------------------

As stated above, OmegaT tags are LTR strings. When translating between
RTL and LTR languages, correctly reading the tags from the source and
entering them properly in the target may require the translator to
toggle between LTR and RTL modes numerous times.

If the document allows, the translator is strongly encouraged to remove
style information from the original document so that as few tags as
possible appear in the OmegaT interface. Follow the indications given in
Hints for tags management. Frequently validate tags (see Tag validation)
and produce translated documents (see below and Menu) at regular
intervals to make it easier to catch any problems that arise. A hint:
translating a plain text version of the text and adding the necessary
style in the relevant application at a later stage may turn out to be
less hassle.

Creating translated RTL documents
---------------------------------

When the translated document is created, its display direction will be
the same as that of the original document. If the original document was
LTR, the display direction of the target document must be changed
manually to RTL in its viewing application. Each output format has
specific ways of dealing with RTL display; check the relevant
application manuals for details.

For .docx files, a number of changes are however done automatically:

-  Paragraphs, sections and tables are set to bidi
-  Runs (text elements) are set to RTL

To avoid changing the target files display parameters each time the
files are opened, it may be possible to change the source file display
parameters such that such parameters are inherited by the target files.
Such modifications are possible in ODF files for example.
