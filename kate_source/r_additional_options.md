# Additional Options

This topic provides an overview on how to download ZIGI from the internet, unzip the files, upload the files to your mainframe, and then run the installer if you're unable to connect your mainframe to GitHub.

If you do not have the option to connect your Mainframe directly to GitHub, you can download the zip files, unzip them, upload them to your mainframe, and then run the installer.

The latest stable version of ZIGI can be downloaded [here](https://github.com/wizardofzos/zigi/wiki).

When running the zginstall.rex script, there are a few prompts asking for a high-level qualifier \(HLQ\) for the ZIGI ISPF data sets to be created under. The ZIGI partitioned data sets are allocated as PDSE partitioned data sets. After the zginstall.rex completes, exit OMVS, return to native ISPF, and then execute the ZGSTAT exec as documented in the zginstall.rex report. That applies the ISPF statistics to the PDS members of ZIGI.

To use the ZG command, it must be copied from the ZIGI.EXEC library into a library in the standard SYSEXEC, or SYSPROC, allocation.

For more information, check out the [ZIGI wiki](https://github.com/wizardofzos/zigi/wiki).

*NEXT TOPIC*: [Using CBTTape](t_using_cbttape.md)

**Parent topic:**[Using Git](t_using_git.md)

