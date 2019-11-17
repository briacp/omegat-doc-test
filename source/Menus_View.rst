View
====

Mark Translated Segments
    If checked, the translated segments will be marked in yellow.

Mark Untranslated Segments
    If checked, the untranslated segments will be marked in violet.

Mark Paragraph delimitations
    If checked, the separations between paragraphs in the source
    document are indicated visually.

Display Source Segments
    If checked, source segments will be shown and marked in green. If
    not checked, source segments will not be shown.

Mark Non-Unique Segments
    If checked, non-unique segments will be marked in pale grey.

Mark Segments with Notes
    If checked, segments with notes will be marked in cyan. This marking
    has priority over Mark Translated Segments and Mark Untranslated
    Segments.

Mark Non-breakable Spaces
    If checked, non-breakable spaces will be displayed with a grey
    background.

Mark Whitespace
    If checked, white spaces will be displayed with a small dot.

Mark Bidirectional Algorithm Control Characters
    This option displays `bidirectional control
    characters <http://www.w3.org/International/questions/qa-bidi-controls>`__

Mark Auto-Populated Segments
    If checked, the background of all segments where the target segment
    has been auto-populated (from TMXs placed in ``/tm/auto`` for
    example) are displayed in colour. The colours are displayed as long
    as the `Save auto-populated
    status <#dialogs.preferences.editor.saveautopopulatedstatus>`__
    option is checked. Usual translations inserted from the auto folder
    are displayed in orange. Other translations, identified specifically
    in the TMX, can be displayed using different colours. For technical
    details, see the `Request For
    Enhancement <http://sourceforge.net/p/omegat/feature-requests/963/>`__.

Aggressive Font Fallback
    Check this option in case OmegaT does not display some glyphs
    properly (even if the fonts containing the relevant glyphs are
    installed on your machine). Note: on Windows it seems that this
    manual font fallback mechanism can interfere with standard font
    fallback, causing undesirable font substitution. For that reason, it
    is OFF by default.

Modification Info
    Setting the Display Modification option to Current segment will
    display the time and the author of the last change in the current
    segment. Setting it to All segments shows this information for all
    segments and None turns this option off.
