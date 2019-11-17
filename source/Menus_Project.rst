Project
=======

New...
    Creates and opens a new project.

Download Team Project...
    Creates a local copy of a remote OmegaT project. See `How to use a
    team project <#howto.useteamproject>`__ for details.

Open...
    Opens a previously created project.

Open Recent Project
    Give access to the ten last edited projects. Clicking on one will
    save the current project, close it and open the other project.

Copy Files to Source Folder...
    Copies the selected files to the ``source`` folder and reloads the
    project to load the new files.

Download MediaWiki Page...
    To translate the contents of a Wikipedia page (for example):

    1. Click the Edit tab on the Wikipedia page.

    2. Copy the URL of the page (ending with action=edit) and paste it
       into OmegaT.

    When you have finished your translation, to import it into
    Wikipedia:

    1. Open the ``.UTF8`` file generated in the ``/target`` folder.

    2. Copy the text and paste it into the translated version of the
       Wikipedia page.

Reload
    Reloads the project to take external changes in source files and
    project settings into account.

    New translation memories placed in the ``/tm`` folder while
    translating are loaded automatically as soon as the cursor moves
    from one segment to another.

Close
    Saves the translation and closes the project.

Save
    Saves the internal translation memory to the hard disk. OmegaT
    automatically saves translations every 3 minutes as well as when you
    close the project or quit OmegaT.

    The interval of 3 minutes can be changed in `Options > Preferences >
    Saving and Output <#dialogs.preferences.savingandoutput>`__.

Commit Source Files
    Uploads to the repository the files that have been added or modified
    locally in the ``source`` directory.

    This function is specific to team projects.

Commit Target Files
    Uploads to the repository the files that have been created locally
    in the ``target`` directory.

    This function is specific to team projects.

Create Translated Documents
    Creates the target documents based on your translation. The created
    target documents are located in the ``target`` folder.

Create Current Translated Document
    Creates the target document corresponding to the current document in
    translation.

Open MED Project...
    Opens a project package in the MED format defined by the EU
    Directorate-General for Translation.

Create MED Projects...
    Converts the current project into a MED package.

Properties...
    Displays `Project properties <#dialogs.projectproperties>`__ dialog
    to edit project languages and folder locations.

Project Files...
    Opens the `Project files window <#windows.projectfiles>`__.

Access Project Contents
    Gives access to the project folders.

    In addition, two menu entries allow opening directly the current
    source and target documents and the writable glossary. The documents
    are opened by the application chosen by the operating system. If the
    documents are not available, the entry is greyed out.

Quit
    Saves the project and quits OmegaT. If you haven't yet saved the
    project, this manually confirms whether you really wish to quit.
