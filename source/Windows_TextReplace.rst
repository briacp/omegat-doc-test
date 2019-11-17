Text Replace
============

Open the Search and replace window with +Ctrl+ +K+ and enter the word or
expression you wish to replace in the *Search for* box.

Then click on *Search* button to display all the corresponding
occurrences.

Enter the new word or phrase (regular expressions are not supported) in
the *Replace with* box, then click one of the following options:

-  **Replace All:** operates replacement of all occurrences (after
   displaying a confirmation window where the number of occurrences is
   shown).

-  **Replace:** operates a "one by one" replacement, by the mean of
   buttons in the **header of the Editor pane**. Click *Replace Next* or
   *Skip*, then end the replacement session with *Finish*.

-  **Close:** close the window without any change.

Search options
--------------

Search options are similar to the ones displayed in `Search
window <#windows.textsearch>`__.

Except one: check **Untranslated** in order to operate Search and
replace also on segments that have not been translated yet.

To make it possible (although Search and replace operates only on
memory), OmegaT will copy the source segment to the target segment
before the replace operation occurs. If no replacement is done to a
given segment, the target segment will be “emptied”, i.e., it will
remain untranslated.
