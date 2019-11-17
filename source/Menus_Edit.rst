Edit
====

This menu displays entries only when a project is open.

Undo Last Action
    Restores the status before the last editing action was taken. This
    command does not work once the modified segment has been validated.

Redo Last Action
    Restores the status before the last editing action was cancelled.
    This command does not work once the modified segment has been
    validated.

Replace With Match or Selection
    Replaces the whole target segment with the currently selected fuzzy
    match (by default the first match is selected).

    If some texts are selected within the fuzzy match, only this
    selection will replace the whole target segment.

Insert Match or Selection
    Inserts the currently selected fuzzy match at the cursor position.
    If part of the target segment has been selected, this function
    overwrites the selected portion.

    If some texts are selected within the fuzzy match, only this
    selection will be inserted at the cursor position.

Replace with Machine Translation
    Replaces the target segment with the translation, provided by the
    selected Machine Translation service. No action is taken, if no
    Machine Translation service has been activated (in Options > Machine
    Translate).

Replace with Source
    Replaces the whole target segment with the source.

Insert Source
    Inserts the source at the cursor position.

Insert Missing Source Tags
    Inserts the source tags (if they where missing) at the cursor
    position.

Insert Next Missing Tag
    Inserts only one tag (among the missing ones) at the cursor
    position.

Export Selection
    Exports the current selection to a text file for processing. If no
    text has been selected, the current source segment is written to
    this file. When the user exits OmegaT, this file is not emptied, in
    order to be consistent with usual clipboard behavior. The exported
    contents are copied to the file ``selection.txt`` located in the
    User's preference files folder.

Create Glossary Entry
    Allows the user create an entry in the default glossary file.

    If you select a text string (in any pane) before pressing +Ctrl+
    +Shift+ +G+ , the text will be pasted by default in the Source term
    field.

    This can apply also to Target term and Commentfields if new
    selections are made and +Ctrl+ +Shift+ +G+ pressed again.

Search Project...
    Opens a new `Search window <#windows.textsearch>`__.

    If you select a text string (in any pane) before pressing +Ctrl+ +F+
    , the text will be pasted by default in the Search for field.

    Pressing +Ctrl+ +Shift+ +F+ displays the last already opened Search
    window (instead of opening a new one).

Search and Replace...
    Opens a new `Search and replace window <#windows.textreplace>`__.

    If you select a text string (in any pane) before pressing +Ctrl+ +K+
    , the text will be pasted by default in the Search for field.

Search Dictionaries
    If `automatic searching in
    dictionaries <#dialogs.preferences.dictionary>`__ is disabled, this
    function allows you to search for the selected word in the
    dictionaries.

Switch case to
    Changes the case of the highlighted text in the target segment to
    the selected option (Lower case, Upper case, Title case or Sentence
    case). Use +Shift+ +F3+ to cycle through the four alternatives. If
    no text is selected, OmegaT selects the word that contains the
    letter immediately to the right of the cursor.

Select Match
    Selects the previous, the next or the Nth fuzzy match displayed in
    the fuzzy match pane to replace or insert it to the segment.

Use as Default Translation
    If there's several alternative translations available for the active
    segment, you can label the alternative selected as the default
    translation. The entry will be greyed, if there's just one
    translation available.

Create Alternative Translation
    The one and the same segment may, depending on the context, require
    different translations. Select this menu item, if the current
    translation does not apply and enter the alternative translation.

Remove Translation
    Deletes the translation and set the segment as untranslated.

Set empty translation
    Define the translation as being empty. In the target document,
    nothing will appear for this segment. In the Editor, the translation
    is displayed as <EMPTY>

Register Identical Translation
    Use this command to register the translation to be identical to the
    source, even if `Allow translation to be equal to
    source <#dialogs.preferences.editor.allowtranslationtobeequaltosource>`__
    is not checked.
