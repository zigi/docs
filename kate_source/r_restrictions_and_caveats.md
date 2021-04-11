# Restrictions and Caveats

This topic explains the restrictions and caveats you should know when using ZIGI.

ZIGI is designed to work under ISPF, using OMVS services, and interfaces to Git.

There are some restrictions and/or caveats that you should be aware of:

-   VSAM, BDAM, and ISAM are not supported.
-   While ZIGI utilizes Git, only those git repositories that are configured for ZIGI can be managed by ZIGI. All others may be cloned, and the conversion utility used after some \(or a lot of\) manual changes.
-   File extensions for the OMVS copy of PDS members is supported with the restriction that each PDS may only have one file extension mapped to it.

Load modules are supported from data sets with RECFM=U. The restriction is that for versions of z/OS prior to 2.4, the following PTFs must be installed:

-   z/OS 2.2 \| UJ01358

-   z/OS 2.3 \| UJ01356


*NEXT TOPIC*: [Starting ZIGI the First Time](t_starting_zigi_the_first_time.md)

