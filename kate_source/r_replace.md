# Replace

Replace replaces all of the current z/OS data sets in the repository with the data in the local repository's OMVS filesystem, including maintaining the ISPF statistics when those data sets were added to the OMVS filesystem. All refreshed partitioned data sets are allocated as PDSE version 2 libraries with the default MAXGEN. If the refreshed library is a PDS, and more than 25% of the members are being updated, then the PDS is reallocated as a PDSE Version 2 with the default MAXGEN. If the refreshed library is a PDSE then it is not reallocated and only the updated members are refreshed.

*NEXT TOPIC*: [Remote Command](r_remote.md)

**Parent topic:**[The ZIGI Current Repository Panel](c_the_zigi_current_repository_panel.md)

