# Convert Repository \(CONVREPO\) Command

This topic explains the functionality of the CONVREPO command.

The convert repository \(CONVREPO\) command converts a repository that has been cloned into your OMVS filesystem into a repository that ZIGI can manage. There are numerous requirements for ZIGI to manage a repository, primarily because Git has no awareness of the z/OS data sets. All Git files are stored in an OMVS filesystem.

A ZIGI-managed repository requires the following:

-   A .zigi directory in the repository root directory.
-   A file with the name of dsn in the .zigi directory with information on the z/OS data sets managed by ZIGI:

    ```screen
    # Default DSORG and DCB info
    * PO FB 80 32720
    SAMPLE.REXX PO VB 255 32760
    SAMPLE.PDS PO FB 80 32760
    SAMPLE.TEXT PS FB 121 27951
    ```

-   Each z/OS sequential data set must have a copy in the repository root directory.
-   Each z/OS partitioned data set must have a directory in the repository root.
-   Each PDS member must have a copy in the directory associated with the full PDS.
-   Only files that are uppercase and conform to z/OS data set naming conventions are accepted by ZIGI to be copied to z/OS.

The conversion process:

1.  Creates a .gitattributes file in the repository root directory if one does not exist. If a .gitattributes exists in the repository then it is untouched, but you should consider updating it with some of the .gitattributes that you can find in ZIGI managed repositories.
2.  Creates a .zigi subdirectory.
3.  Creates a .zigi/dsn file with a set of defaults.
4.  Identifies files in the repository root that conform to z/OS data set naming conventions, after being translated to uppercase, and copies them to z/OS data sets using the HLQ defined when the repository was cloned.
5.  Identifies directories in the repository root that conform to z/OS data set naming conventions after being translated to uppercase.
    1.  Creates a PDS in z/OS.
    2.  Renames the members within to remove any suffix to files with uppercase names assuming the file conforms to z/OS PDS member naming conventions.
    3.  Copies renamed files to the PDS as members.
6.  Files that end with .bin are treated as binary files and the .bin suffix is removed when copied to z/OS.

*NEXT TOPIC*: [Extract Command](r_extract.md)

**Parent topic:**[The ZIGI Current Repository Panel](c_the_zigi_current_repository_panel.md)

