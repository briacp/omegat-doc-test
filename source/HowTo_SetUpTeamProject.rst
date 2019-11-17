Set up a Team Project
=====================

Setting up a team project requires some knowledge of servers and the SVN
or Git versioning systems. It should thus be carried out by a project
manager, a project leader or a localisation engineer.

As plenty of information about SVN and Git is easily available, we won't
describe how they work here, but only how OmegaT works with them.

Step 1: Create an empty project on a server
-------------------------------------------

**Creating an empty project on a server**

1. Create an SVN or Git repository on a server that will be accessible
   by the translators.

2. Create a local copy of the repository (``check
           out`` with SVN, ``clone`` with Git).

3. Create a new, empty OmegaT project in the local repository. This can
   be done in two ways:

   -  Project > New...

   -  on the command line: ``java -jar OmegaT.jar team init
                  [lang1] [lang2]``

4. Add the new OmegaT project to the versioning system (``add`` with SVN
   and Git)

   Note: If the project was created with the command line in step 3,
   this step has already been done by the program.

5. Publish the new OmegaT project on the server (``commit`` with SVN,
   ``commit`` followed by ``push`` with Git).

**Specific parameters**

If the project uses specific filters and segmentation parameters, both
the ``filters.xml`` and ``segmentation.conf`` files must be added to the
versioning system and published on the server.

Step 2: Add files to translate and other resources
--------------------------------------------------

Use an SVN or Git client to add the files to translate.

This can also be done within OmegaT:

1. copy the files to the ``/source`` folder

2. use Project > Commit Source Files

To add other resources (dictionaries, TMXs or glossaries), use an SVN or
Git client.

To **delete files**, use an SVN or Git client. These files won't be
deleted automatically on the translator's side: you must ask them to
delete the files manually.

Note that only two files are modified by OmegaT during translation:

-  ``omegat/project_save.tmx``

-  ``glossary/glossary.txt``

All other files are read-only. If the translator attempts to modify
them, they will go back to their original state whenever the project is
opened, closed, saved or reloaded.

Step 3: Send an invitation to the translator
--------------------------------------------

Once the project is set up on the server, the project manager can invite
the translator to work on it in either of two different ways:

-  sending the URL of the project and asking the translator to create a
   local copy with Project > Download Team Project.

-  sending an ``omegat.project`` file containing a reference to the URL
   and asking the translator to copy it into a dedicated folder and open
   it with OmegaT.

   The reference to the URL is specified as below (here to a Git
   repository):

   ::

       <repositories>
        <repository type="git" url="https://repo_for_OmegaT_team_project.git">
         <mapping local="" repository=""/>
        </repository>
       </repositories>

In both cases, the project manager must send the translator their ID and
password to access the repository.

**Checking statistics**

The Project Manager should check with the translator that the statistics
are identical on both sides (server side and translator side).

If there are any differences, check that the ``filters.xml`` and
``segmentation.conf`` files are under version control.

Special case: minimal sharing
-----------------------------

The process above describes the usual case, where the project manager
wants to have full control of the project and where the files (and the
statistics) are identical on both sides (server side and translator
side).

OmegaT team projects can also be set up in a different way, where
several translators share the project\_save.tmx file but not the source
files.

In this case, the procedure is the same, but the project manager does
not add files to the /source folder.

Mapping parameters
------------------

repository type
    This can be either http (which includes https), svn or git.

repository url
    Remote location of the files to translate.

mapping local
    Name of the local folder or file, relative to the root of the OmegaT
    project.

mapping repository
    Name of the remote folder or file, relative to the repository url.

excludes
    Add patterns using wildcards (Apache Ant style): \*, ?, \*\*

    Example: ``**/.ini/**``

includes
    As above.

    Example: ``**/*.docx`` to add all .docx files, wherever they are
    located in the project.

    The inclusion rules take priority over the exclusion rules.

Example mappings
----------------

::

    <repositories>
     <repository type="svn" url="https://repo_for_OmegaT_team_project">
      <mapping local="" repository=""/>
     </repository>
    </repositories>

All the contents of ``https://repo_for_OmegaT_team_project`` are mapped
to the local OmegaT project

::

    <repositories>
     <repository type="svn" url="https://repo_for_All_OmegaT_team_projects">
      <mapping local="" repository="En-US_DE_project"/>
     </repository>
    </repositories>

All the contents of
``https://repo_for_All_OmegaT_team_projects/En-US_DE_project`` are
mapped to the local OmegaT project.

::

    <repository type="http" url="https://github.com/omegat-org/omegat/raw/master/">
                <mapping local="source/Bundle.properties" repository="src/org/omegat/Bundle.properties"/>
                </repository>

The remote file
``https://github.com/omegat-org/omegat/raw/master/src/org/omegat/Bundle.properties``
is mapped to the local file ``source/Bundle.properties``.

::

    <repository type="http" url="https://github.com/omegat-org/omegat/raw/master/">
                <mapping local="source/Bundle.properties" repository="src/org/omegat/Bundle.properties"/>
                   <mapping local="source/readme_tr.txt" repository="release/readme.txt"/>
                </repository>

The remote file
``https://github.com/omegat-org/omegat/raw/master/release/readme.txt``
is mapped to the local file ``source/readme_tr.txt``.

This makes it possible to rename the file to be translated.
