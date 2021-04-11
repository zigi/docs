# Creating a New Repository \(Local and Remote\)

There are two ways of creating a \(Git-based\) repository with ZIGI:

-   Cloning a remote repository or creating one from scratch locally.
-   Using the create command to create a new \(local\) repository.

This performs a git init repoName in the chosen directory. A basic .gitattributes is created and added/committed to your repository. This is there to ensure that the encoding of the various Git-managed files are in the correct format. After creating the local repo \(ZIGI takes care of your .gitattributes file\) you can ADD data sets to the repository. \(See [AddAll Command](r_addall.md) command\).

Adding files to ZIGI is not the same thing as adding them to the Git repository. Once a data set has been added to ZIGI, the data sets \(in file-format\) are only available in the working-space of the Git repository. \(They are present in /repofolder/reponame\).

Adding to the Git-repo is done via the add \(A\) line command.

*NEXT TOPIC:* [Adding a Remote Repository](r_adding_a_remote_repository.md)

**Parent topic:**[Typical ZIGI Activities](c_typical_zigi_activities.md)

