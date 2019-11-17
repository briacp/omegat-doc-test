Prevent data loss
=================

OmegaT is a robust application. However, you should take precautions
against data loss when using OmegaT, just as with any other application.
When you translate your files, OmegaT stores all your progress in the
translation memory ``project_save.tmx`` that resides in the project's
``/omegat`` subfolder.

OmegaT also backs up the translation memory to
project\_save.tmx.YEARMMDDHHNN.bak in the same subfolder each time a
project is opened or reloaded. YEAR is the 4-digit year, MM is the
month, DD the day of the month, and HH and NN are the hours and minutes
when the previous translation memory was saved.

If you believe that you have lost translation data, you can use the
following procedure to restore the project to its most recently saved
state, usually not older than approximately 10 minutes or so:

1. close the project

2. rename the current ``project_save.tmx ``\ file (e.g. to
   ``project_save.tmx.temporary``)

3. select the backup translation memory that is the most likely to
   contain the data you are looking for

4. rename it ``project_save.tmx``

5. open the project

To avoid losing important data:

-  Make regular copies of the file /omegat/project\_save.tmx to backup
   media, such as CD or DVD.

-  Until you are familiar with OmegaT, create translated files at
   regular intervals and check that the translated file contains the
   latest version of your translation.

-  Take particular care when making changes to the files in ``/source``
   while in the middle of a project. If the source file is modified
   after you have begun translating, OmegaT may be unable to find a
   segment that you have already translated.

-  Use these Help texts to get started. Should you run into problems,
   post a message in the `OmegaT user
   group <https://groups.yahoo.com/neo/groups/OmegaT/info>`__. Do not
   hesitate to post in the language you feel the most familiar with.
