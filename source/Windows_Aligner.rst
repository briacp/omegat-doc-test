Aligner
=======

Alignment involves creating a bilingual translation memory from
monolingual documents that have already been translated.

To access this window, select Tools > Align Files....

Step 1: Adjust the alignment parameters
---------------------------------------

If the alignment looks as if it could be improved, try changing the
parameters. In most cases, the lower the Average score is, better the
alignment will be.

In Heapwise mode, the texts are evaluated globally. In Parsewise mode,
they are evaluated segment by segment.

Use ID comparison mode to align Key=Value texts. This works even if the
keys are not in the same order in the two files, and/or if the two files
do not contain the same amount of information. This option only appears
if both the selected files are recognised as Key=Value files.

The Viterbi and Forward-Backward algorithms are two different
calculation methods. Choose the one that provides the best results.

Click Continue to access the next step.

Step 2: Make manual corrections
-------------------------------

After the automatic process, the alignment of two files generally
requires manual corrections.

Translation units are located in cells in the two last columns.

To align two segments on the same line:

1. Select the first segment.

2. Press the space bar (shortcut for Edit > Start Pinpoint Align).

3. Click in the other column on the translation corresponding to the
   first segment.

After several of these operations, select Edit > Realign pending to
update the alignment of the other segments.

To modify the position of one or more segments individually, select the
segment(s) and press ``U`` (Move Up) or ``D`` (Move Down).

Only rows with the Keep box ticked in the first column will be included
when the translation memory is created.

When the two columns are sufficiently aligned, click Save TMX... to
create the resulting translation memory.
