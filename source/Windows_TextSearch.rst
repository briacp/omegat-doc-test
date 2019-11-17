Text Search
===========

Open the Search window with +Ctrl+ +F+ and enter the word or phrase you
wish to search for in the *Search for* box.

Alternatively, you can select a word or phrase in the Editor pane, Fuzzy
matches pane or Glossary pane and hit +Ctrl+ +F+ . The word or phrase is
entered in the *Search for* box automatically. You can have several
Search windows open at the same time, but close them when they are no
longer needed so that they do not clutter your desktop.

Click the dropdown arrow of the *Search for* box to access the last 10
searches.

The Search window has its own menus:

-  File > Search for selection ( +Ctrl+ +F+ ): refocus on the search
   field and select all its contents.

-  File > Close ( +Ctrl+ +W+ ): close the search window (in the same way
   as Esc)

-  Edit > Insert source ( +Ctrl+ +Shift+ +I+ ): insert current segment
   source.

-  Edit > Replace with source ( +Ctrl+ +Shift+ +R+ ): replace with
   current segment source.

-  Edit > Create Glossary Entry ( +Ctrl+ +Shift+ +G+ ): add a new
   glossary item.

Using wild cards
----------------

In both exact and keyword searches, the wild card search characters '\*'
and '?' can be used. They have the meaning, familiar to Word users:

-  '\*' matches zero or more characters, from the current position in a
   given word to its end. The search term ``'run*'`` for example would
   match words ``'run'``, ``'runs'`` and ``'running'``.

-  '?' matches any single character. For instance, ``'run?'`` would
   match the word ``'runs'`` and ``'runn'`` in the word ``'running'``.

The matches will be displayed in bold blue. Note that '\*' and '?' have
special meaning in regular expressions, so wild card search, as
described here, applies to exact and keyword search only (see below).

Search methods and options
--------------------------

Select the method using the radio buttons. The following search methods
are available:

exact search
    Search for segments containing the exact string you specified. An
    exact search looks for a phrase, i.e. if several words are entered,
    they are found only if they occur in exactly that sequence.
    Searching for ``open file`` will thus find all occurrences of the
    string *``open
              file``*, but not *``file
              opened``* or *``open input
              file``*.

keyword search
    Search for segments containing all keywords you specified, in any
    order. Select keyword search to search for any number of individual
    full words, in any order. OmegaT displays a list of all segments
    containing all of the words specified. Keyword searches are similar
    to a search "with all of the words" in an Internet search engine
    such as Google (AND logic). Using keyword search with
    *``open file``* will thus find all occurrences of the string *``open
              file``,* as well as *``file
              opened``, ``open input file``, ``file
              may not be safe to open``*, etc.

**regular expressions**
    The search string will be treated as a regular expression. The
    search string - [a-zA-Z]+[öäüqwß] - in the example above for
    instance looks for words in the target segment, containing
    questionable characters from German keyboard. `Regular
    expressions <#appendix.regexp>`__ are a powerful way to look for
    instances of a string.

Additionally to one of the methods above you can select the following:

-  **case sensitive**: the search will be performed for the exact string
   specified; i.e. capitalization is observed.

-  **Space matches nbsp**: when this option is checked, a space
   character put in search entry can match either a normal space
   character or a non-breacking space (\\u00A) character.

-  **in source:**\ search in the source segments

-  **in translations:**\ search in the target segments

-  **in notes:**\ search in notes to segments

-  **in comments:**\ search in comments to segments

-  **Translated or untranslated:**\ search in both translated and
   untranslated segments.

-  **Translated:**\ search only in translated segments.

-  **Untranslated:**\ search only in untranslated segments.

-  **Display: all matching segments:**\ if checked, all the segments are
   displayed one by one, even if they are present several times in the
   same document or in different documents.

-  **Display: file names:**\ if checked, the name of the file where each
   segment is found is displayed above each result.

-  **Search in Project**: check *Memory* to include the project memory
   (project\_save.tmx file) in the search. Check *TMs* to include the
   translation memories located in the ``tm`` folder in the search.
   Check *Glossaries* to include the glossaries located in the
   ``glossary`` folder in the search.

-  **Search in Files:**\ search in a single file or a folder containing
   a set of files. When searching through files (as opposed to
   translation memories), OmegaT restricts the search to files in source
   file formats. Consequently, although OmegaT is quite able to
   handle\ `` tmx`` files, it does not include them in the Search files
   search.

If you click on the button Advanced options additional criteria (author
or changer of the translation, date translated, excluding orphan
segments, etc) can be selected. When *Full/Half width char insensitive*
option is checked, searches for fullwidth forms (CJK characters) will
match halfwidth forms and vice versa.

Search results display
----------------------

Pressing the search button after entering a string in the search field
displays all the segments in the project that include the entered
string. As OmegaT handles identical segments as one single entity, only
the first unique segment is shown. The segments are displayed in order
of appearance in the project. Translated segments are displayed with the
original text at the top and the translated text at the bottom,
untranslated segments are displayed as the source only.

Double-clicking on a segment opens it in the Editor for modifications
(one single click does it when **Auto-sync with Editor** option is
checked). You can then switch back to the Search window for the next
segment found, for instance to check and, if necessary, correct the
terminology.

In the Search window, you can use standard shortcuts ( +Ctrl+ +N+ ,
+Ctrl+ +P+ ) to move from one segment to another.

You may have several Search windows open at the same time. You can
quickly see their contents by looking at their title: it will contain
the search term used.

Filter entries in editor according to search
--------------------------------------------

For easier navigation in the search result set, you can apply the search
to the editor. Press the **Filter** button on the bottom to limit the
shown entries in the editor window to those that match the current
search. You can use normal navigation to go to e.g. the next
(untranslated) segment that matches the search criteria.

NB:

-  A search may be limited to 1000 items, so if you search on a common
   phrase, the editor then shows only those 1000 matching entries, and
   not all entries that match the search criteria.

-  A file might have no matching entries, so it will show empty.

-  If a search removes duplicates, those duplicates will not be in the
   Editor.

To remove a filter, press the **Remove filter** button, or reload a
project.
