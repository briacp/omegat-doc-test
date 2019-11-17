Shortcuts customization
=======================

Shortcuts customization
=======================

Most of the items that appear in the main menu can have a new shortcut
assigned. You can change the already assigned shortcuts and add new
shortcuts by putting a shortcut definition file in your OmegaT
preferences folder (accessible by Options > Access Configuration Folder
menu).

The shortcut definition file must be named
``MainMenuShortcuts.properties`` and must contain at most one shortcut
definition per line. Empty lines are accepted and comment lines should
start with "//". Anything after the "//" will be ignored.

Once the ``MainMenuShortcuts.properties`` file is modified, OmegaT must
be relaunched to take the new shortcuts into account.

The shortcut definition syntax is the following: ``<menu item
    code>=<shortcut>``, where *<menu item code>* is a code taken from
the tables below and *<shortcut>* is a combination of pressed keys
specified by the user [1]_.

<shortcut> must be of the following form: 0 or more ``<modifier>``
followed by 0 or 1 ``<event>`` followed by 1 ``<key>``, where:

-  ``<modifier>`` can be: *shift*, *control*, *ctrl*, *meta*\  [2]_,
   *alt*, *altGraph*

-  ``<event>`` can be: *typed*, *pressed*, *released*

-  and ``<key>`` can be any key available on your keyboard [3]_.

For example, in the default OmegaT shortcuts [4]_, one can find:

-  ``projectOpenMenuItem=ctrl O``

-  ``editCreateGlossaryEntryMenuItem=ctrl shift G``

The first is the shortcut for Open Project, the second for Create
Glossary Entry.

If you want to use +Shift+ +Ctrl+ +O+ to open a project, modify your
``MainMenuShortcuts.properties`` as follows:\ ``
    ``

``projectOpenMenuItem=shift ctrl O``.

If you are on a Mac and you want to add a +Shift+ +Command+ +S+ shortcut
to Tools > Statistics, add the following line to your
``MainMenuShortcuts.properties``:````

`` toolsShowStatisticsStandardMenuItem=shift meta
    S``

Save then the file and relaunch OmegaT. Your new shortcuts should now
appear next to the menu items you have modified. If they do not conflict
with system shortcuts, they should be available from within OmegaT.

Project Menu
============

+---------------------------------------------------+--------------------+----------------------------------------------+
| Menu Item                                         | Default shortcut   | Menu Item Code                               |
+===================================================+====================+==============================================+
| New                                               | Ctrl+Shift+N       | projectNewMenuItem                           |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Download Team Project                             |                    | projectTeamNewMenuItem                       |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Open                                              | Ctrl+O             | projectOpenMenuItem                          |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Open Recent Project                               |                    | projectOpenRecentMenuItem                    |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Copy Files to Source Folder...                    |                    | projectImportMenuItem                        |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Download MediaWiki Page...                        |                    | projectWikiImportMenuItem                    |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Reload                                            | F5                 | projectReloadMenuItem                        |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Close                                             | Ctrl+Shift+W       | projectCloseMenuItem                         |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Save                                              | Ctrl+S             | projectSaveMenuItem                          |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Create Translated Documents                       | Ctrl+D             | projectCompileMenuItem                       |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Create Current Translated Documents               | Ctrl+Shift+D       | projectSingleCompileMenuItem                 |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Properties...                                     | Ctrl+E             | projectEditMenuItem                          |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Project Files...                                  | Ctrl+L             | viewFileListMenuItem                         |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Access Project Contents/Root                      |                    | projectAccessRootMenuItem                    |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Access Project Contents/Dictionaries              |                    | projectAccessDictionaryMenuItem              |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Access Project Contents/Glossaries                |                    | projectAccessGlossaryMenuItem                |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Access Project Contents/Source Files              |                    | projectAccessSourceMenuItem                  |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Access Project Contents/Target Files              |                    | projectAccessTargetMenuItem                  |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Access Project Contents/Current Source Document   |                    | projectAccessCurrentSourceDocumentMenuItem   |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Access Project Contents/Current Target Document   |                    | projectAccessCurrentTargetDocumentMenuItem   |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Access Project Contents/Writeable Glossary        |                    | projectAccessWriteableGlossaryMenuItem       |
+---------------------------------------------------+--------------------+----------------------------------------------+
| Quit                                              | Ctrl+Q             | projectExitMenuItem                          |
+---------------------------------------------------+--------------------+----------------------------------------------+

Table: Project Menu

Edit Menu
=========

+------------------------------------+--------------------+-------------------------------------------+
| Menu Item                          | Default shortcut   | Menu Item Code                            |
+====================================+====================+===========================================+
| Undo Last Action                   | Ctrl+Z             | editUndoMenuItem                          |
+------------------------------------+--------------------+-------------------------------------------+
| Redo Last Action                   | Ctrl+Y             | editRedoMenuItem                          |
+------------------------------------+--------------------+-------------------------------------------+
| Replace With Match or Selection    | Ctrl+R             | editOverwriteTranslationMenuItem          |
+------------------------------------+--------------------+-------------------------------------------+
| Insert Match or Selection          | Ctrl+I             | editInsertTranslationMenuItem             |
+------------------------------------+--------------------+-------------------------------------------+
| Replace with Machine Translation   | Ctrl+M             | editOverwriteMachineTranslationMenuItem   |
+------------------------------------+--------------------+-------------------------------------------+
| Replace With Source                | Ctrl+Shift+R       | editOverwriteSourceMenuItem               |
+------------------------------------+--------------------+-------------------------------------------+
| Insert Source                      | Ctrl+Shift+I       | editInsertSourceMenuItem                  |
+------------------------------------+--------------------+-------------------------------------------+
| Insert Missing Source Tags         | Ctrl+Shift+T       | editTagPainterMenuItem                    |
+------------------------------------+--------------------+-------------------------------------------+
| Insert Next Missing Tag            | Ctrl+T             | editTagNextMissedMenuItem                 |
+------------------------------------+--------------------+-------------------------------------------+
| Export Selection                   | Ctrl+Shift+C       | editExportSelectionMenuItem               |
+------------------------------------+--------------------+-------------------------------------------+
| Create Glossary Entry              | Ctrl+Shift+G       | editCreateGlossaryEntryMenuItem           |
+------------------------------------+--------------------+-------------------------------------------+
| Search Project...                  | Ctrl+F             | editFindInProjectMenuItem                 |
+------------------------------------+--------------------+-------------------------------------------+
|                                    | Ctrl+Shift+F       | findInProjectReuseLastWindow              |
+------------------------------------+--------------------+-------------------------------------------+
| Search and Replace...              | Ctrl+K             | editReplaceInProjectMenuItem              |
+------------------------------------+--------------------+-------------------------------------------+
| Switch Case To/Lower Case          |                    | lowerCaseMenuItem                         |
+------------------------------------+--------------------+-------------------------------------------+
| Switch Case To/Upper Case          |                    | upperCaseMenuItem                         |
+------------------------------------+--------------------+-------------------------------------------+
| Switch Case To/Title Case          |                    | titleCaseMenuItem                         |
+------------------------------------+--------------------+-------------------------------------------+
| Switch Case To/Sentence Case       |                    | sentenceCaseMenuItem                      |
+------------------------------------+--------------------+-------------------------------------------+
| Switch Case To/Cycle               | Shift+F3           | cycleSwitchCaseMenuItem                   |
+------------------------------------+--------------------+-------------------------------------------+
| Select Previous Match              | Ctrl+↑             | editSelectFuzzyPrevMenuItem               |
+------------------------------------+--------------------+-------------------------------------------+
| Select Next Match                  | Ctrl+↓             | editSelectFuzzyNextMenuItem               |
+------------------------------------+--------------------+-------------------------------------------+
| Select Match #1                    | Ctrl+1             | editSelectFuzzy1MenuItem                  |
+------------------------------------+--------------------+-------------------------------------------+
| Select Match #2                    | Ctrl+2             | editSelectFuzzy2MenuItem                  |
+------------------------------------+--------------------+-------------------------------------------+
| Select Match #3                    | Ctrl+3             | editSelectFuzzy3MenuItem                  |
+------------------------------------+--------------------+-------------------------------------------+
| Select Match #4                    | Ctrl+4             | editSelectFuzzy4MenuItem                  |
+------------------------------------+--------------------+-------------------------------------------+
| Select Match #5                    | Ctrl+5             | editSelectFuzzy5MenuItem                  |
+------------------------------------+--------------------+-------------------------------------------+
| Use as Default Translation         |                    | editMultipleDefault                       |
+------------------------------------+--------------------+-------------------------------------------+
| Create Alternative Translation     |                    | editMultipleAlternate                     |
+------------------------------------+--------------------+-------------------------------------------+
| Remove translation                 |                    | editRegisterUntranslatedMenuItem          |
+------------------------------------+--------------------+-------------------------------------------+
| Set empty translation              |                    | editRegisterEmptyMenuItem                 |
+------------------------------------+--------------------+-------------------------------------------+
| Register Identical Translation     | Ctrl+Shift+S       | editRegisterIdenticalMenuItem             |
+------------------------------------+--------------------+-------------------------------------------+

Table: Edit Menu

GoTo Menu
=========

+-----------------------------+------------------------------------+--------------------------------+
| Menu Item                   | Default shortcut                   | Menu Item Code                 |
+=============================+====================================+================================+
| Next Untranslated Segment   | Ctrl+U                             | gotoNextUntranslatedMenuItem   |
+-----------------------------+------------------------------------+--------------------------------+
| Next Translated Segment     | Ctrl+Shift+U                       | gotoNextTranslatedMenuItem     |
+-----------------------------+------------------------------------+--------------------------------+
| Next Segment                | Ctrl+N or Enter or Tab             | gotoNextSegmentMenuItem        |
+-----------------------------+------------------------------------+--------------------------------+
| Previous Segment            | Ctrl+P or Ctrl+Enter or Ctrl+Tab   | gotoPreviousSegmentMenuItem    |
+-----------------------------+------------------------------------+--------------------------------+
| Segment number...           | Ctrl+J                             | gotoSegmentMenuItem            |
+-----------------------------+------------------------------------+--------------------------------+
| Next Note                   |                                    | gotoNextNoteMenuItem           |
+-----------------------------+------------------------------------+--------------------------------+
| Previous Note               |                                    | gotoPreviousNoteMenuItem       |
+-----------------------------+------------------------------------+--------------------------------+
| Next Unique Segment         | Ctrl+Shift+Q                       | gotoNextUniqueMenuItem         |
+-----------------------------+------------------------------------+--------------------------------+
| Source of Selected Match    | Ctrl+Shift+M                       | gotoMatchSourceSegment         |
+-----------------------------+------------------------------------+--------------------------------+
| Forward in history...       | Ctrl+Shift+N                       | gotoHistoryForwardMenuItem     |
+-----------------------------+------------------------------------+--------------------------------+
| Back in history...          | Ctrl+Shift+P                       | gotoHistoryBackMenuItem        |
+-----------------------------+------------------------------------+--------------------------------+

Table: GoTo Menu

View Menu
=========

+---------------------------------------------------+--------------------+----------------------------------------------------------+
| Menu Item                                         | Default shortcut   | Menu Item Code                                           |
+===================================================+====================+==========================================================+
| Mark Translated Segments                          |                    | viewMarkTranslatedSegmentsCheckBoxMenuItem               |
+---------------------------------------------------+--------------------+----------------------------------------------------------+
| Mark Untranslated Segments                        |                    | viewMarkUntranslatedSegmentsCheckBoxMenuItem             |
+---------------------------------------------------+--------------------+----------------------------------------------------------+
| Display Source Segments                           |                    | viewDisplaySegmentSourceCheckBoxMenuItem                 |
+---------------------------------------------------+--------------------+----------------------------------------------------------+
| Mark Non-Unique Segments                          |                    | viewMarkNonUniqueSegmentsCheckBoxMenuItem                |
+---------------------------------------------------+--------------------+----------------------------------------------------------+
| Mark Segments with Notes                          |                    | viewMarkNotedSegmentsCheckBoxMenuItem                    |
+---------------------------------------------------+--------------------+----------------------------------------------------------+
| Mark Non-breakable Spaces                         |                    | viewMarkNBSPCheckBoxMenuItem                             |
+---------------------------------------------------+--------------------+----------------------------------------------------------+
| Mark Whitespace                                   |                    | viewMarkWhitespaceCheckBoxMenuItem                       |
+---------------------------------------------------+--------------------+----------------------------------------------------------+
| Mark Bidirectional Algorithm Control Characters   |                    | viewMarkBidiCheckBoxMenuItem                             |
+---------------------------------------------------+--------------------+----------------------------------------------------------+
| Mark Auto-Populated Segments                      |                    | viewMarkAutoPopulatedCheckBoxMenuItem                    |
+---------------------------------------------------+--------------------+----------------------------------------------------------+
| Modification Info/Display None                    |                    | viewDisplayModificationInfoNoneRadioButtonMenuItem       |
+---------------------------------------------------+--------------------+----------------------------------------------------------+
| Modification Info/Display Selected                |                    | viewDisplayModificationInfoSelectedRadioButtonMenuItem   |
+---------------------------------------------------+--------------------+----------------------------------------------------------+
| Modification Info/Display All                     |                    | viewDisplayModificationInfoAllRadioButtonMenuItem        |
+---------------------------------------------------+--------------------+----------------------------------------------------------+

Table: View Menu

Tools Menu
==========

+--------------------------------------+--------------------+---------------------------------------------+
| Menu Item                            | Default shortcut   | Menu Item Code                              |
+======================================+====================+=============================================+
| Validate Tags                        | Ctrl+Shift+V       | toolsValidateTagsMenuItem                   |
+--------------------------------------+--------------------+---------------------------------------------+
| Validate Tags for Current Document   |                    | toolsSingleValidateTagsMenuItem             |
+--------------------------------------+--------------------+---------------------------------------------+
| Statistics                           |                    | toolsShowStatisticsStandardMenuItem         |
+--------------------------------------+--------------------+---------------------------------------------+
| Match Statistics                     |                    | toolsShowStatisticsMatchesMenuItem          |
+--------------------------------------+--------------------+---------------------------------------------+
| Match Statistics per File            |                    | toolsShowStatisticsMatchesPerFileMenuItem   |
+--------------------------------------+--------------------+---------------------------------------------+

Table: Tools Menu

Options Menu
============

+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Menu Item                                                 | Default shortcut   | Menu Item Code                                     |
+===========================================================+====================+====================================================+
| Use TAB To Advance                                        |                    | optionsTabAdvanceCheckBoxMenuItem                  |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Always Confirm Quit                                       |                    | optionsAlwaysConfirmQuitCheckBoxMenuItem           |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Glossary/Display Context Description for TBX Glossaries   |                    | optionsGlossaryTBXDisplayContextCheckBoxMenuItem   |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Use Terms Appearing Separately in the Source Text         |                    | optionsGlossaryExactMatchCheckBoxMenuItem          |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Glossary/Use Stemming for Glossary Entries                |                    | optionsGlossaryStemmingCheckBoxMenuItem            |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| TransTips/Enable Transtips                                |                    | optionsTransTipsEnableMenuItem                     |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Auto-completion/Show Relevant Suggestions Automatically   |                    | optionsAutoCompleteShowAutomaticallyItem           |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Auto-completion/Glossary...                               |                    | optionsAutoCompleteGlossaryMenuItem                |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Auto-completion/Auto-text...                              |                    | optionsAutoCompleteAutoTextMenuItem                |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Auto-completion/Character Table...                        |                    | optionsAutoCompleteCharTableMenuItem               |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Font...                                                   |                    | optionsFontSelectionMenuItem                       |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Custom Colours...                                         |                    | optionsColorsSelectionMenuItem                     |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| File Filters...                                           |                    | optionsSetupFileFiltersMenuItem                    |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Segmentation...                                           |                    | optionsSentsegMenuItem                             |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Spell checking...                                         |                    | optionsSpellCheckMenuItem                          |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Editing Behavior...                                       |                    | optionsWorkflowMenuItem                            |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Tag Processing...                                         |                    | optionsTagValidationMenuItem                       |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Team...                                                   |                    | optionsTeamMenuItem                                |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| External TMXs...                                          |                    | optionsExtTMXMenuItem                              |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| View...                                                   |                    | optionsViewOptionsMenuItem                         |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Saving and Output...                                      |                    | optionsSaveOptionsMenuItem                         |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Proxy Login...                                            |                    | optionsViewOptionsMenuLoginItem                    |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Restore Main Window                                       |                    | optionsRestoreGUIMenuItem                          |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+
| Access Configuration Folder                               |                    | optionsAccessConfigDirMenuItem                     |
+-----------------------------------------------------------+--------------------+----------------------------------------------------+

Table: Options Menu

Help Menu
=========

+-------------------+--------------------+---------------------------+
| Menu Item         | Default shortcut   | Menu Item Code            |
+===================+====================+===========================+
| User Manual...    | F1                 | helpContentsMenuItem      |
+-------------------+--------------------+---------------------------+
| About...          |                    | helpAboutMenuItem         |
+-------------------+--------------------+---------------------------+
| Last Changes...   |                    | helpLastChangesMenuItem   |
+-------------------+--------------------+---------------------------+
| Log...            |                    | helpLogMenuItem           |
+-------------------+--------------------+---------------------------+

Table: Help Menu

.. [1]
   The full syntax for keystrokes (shortcuts) is defined in the
   following Java 1.6 documentation from Oracle (bottom of page): `Java
   1.6 keystrokes
   shortcuts <http://docs.oracle.com/javase/6/docs/api/javax/swing/KeyStroke.html>`__

.. [2]
   On the Mac, the modifier *meta* must be used to specify the *command*
   key.

.. [3]
   The possible keyevents (keys) are listed in the following Java 1.6
   documentation from Oracle: `Java 1.6 keyEvents
   description <http://docs.oracle.com/javase/6/docs/api/java/awt/event/KeyEvent.html>`__

.. [4]
   The default OmegaT shortcuts are available from Sourceforge: `Default
   OmegaT
   Shortcuts <https://sourceforge.net/p/omegat/svn/HEAD/tree/trunk/src/org/omegat/gui/main/MainMenuShortcuts.properties>`__

   The default OmegaT shortcuts for the Mac are also available from
   Sourceforge, they all use "meta" instead of "ctrl": `Default OmegaT
   Shortcuts for the
   Mac <https://sourceforge.net/p/omegat/svn/HEAD/tree/trunk/src/org/omegat/gui/main/MainMenuShortcuts.mac.properties>`__
