# Using CBTTape

1.  Download file 997 to your workstation and unzip.

2.  Binary upload the resulting XMIT file to z/OS using RECFM=FB LRECL=80.

3.  From TSO, or ISPF Option 6, issue RECEIVE INDS\(upload-file-name.xmit\).

    1.  Enter a data set name or take the default.
4.  Open the resulting PDS and execute the $INSTALL member, which receives the EXEC and PANELS members into full partitioned data sets.

5.  Edit the PDS member STUB to customize for your site, and then copy it into a library in your SYSPROC or SYSEXEC allocations under the name ZIGI.

6.  Start ZIGI from any ISPF Panel by entering TSO %ZIGI.

7.  To use the ZG command, it must be copied from the ZIGI.EXEC library into a library in the standard SYSEXEC, or SYSPROC, allocation.


Check the [Updates](http://www.cbttape.org/updates.htm) page on the [CBTTape website](http://www.cbttape.org/) for the latest release, and if you do not see it there, then go to the **CBT** page under **Downloads** on the left-hand side.

**Tip:** You can also download ZIGI from [this page](https://www.cbttape.org/) in file 997.

*NEXT TOPIC*: [Dovetail Enhancements](r_dovetail_enhancements.md)

**Parent topic:**[Installing ZIGI](c_installing_zigi.md)

