Use a Team Project
==================

OmegaT team projects must first be `set up <#howto.setupteamproject>`__
on a server.

To use a team project for the first time, follow the procedure provided
by the project manager.

Once the project has been opened, translation proceeds in the same way
as for a non-team project, except the following points.

**Automatic saving**

Every 3 minutes (by default), the local project is synchronised with the
remote repository so that the project manager or other translators can
see and use translations added during that period.

The interval of 3 minutes can be changed in `Options > Preferences >
Saving and Output <#dialogs.preferences.savingandoutput>`__.

**Synchronised files**

Whenever the project is automatically saved, but also when it is opened,
closed and reloaded, only two files are actually synchronised:

-  ``omegat/project_save.tmx``

-  ``glossary/glossary.txt``

All other files will be replaced by the files in the remote repository.

**Adding new source files**

To add a new source file:

1. copy the files to the ``/source`` folder

2. use Project > Commit Source Files

Existing source files can be modified, but the commit operation must be
carried out before an automatic save and before the project is reloaded
or closed.

**Deleting source files**

Files must be deleted first by the project manager, and then locally.

**Changing segmentation rules or file filters**

Project parameters must be changed by the project manager.

**Working offline**

A team project can be opened and translated offline. All the changes
will be synchronised the next time a connection is available.

To work offline:

-  Disconnect from the network before opening the project,

-  or open the project with the command line using the ``--no-team``
   option.
