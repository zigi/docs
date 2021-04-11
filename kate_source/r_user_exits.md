# Appendix D: User Exits

ZIGI version 3.10 includes new user exits. All exits are provided as samples that must be updated by each site and then installed using the correct exit name.

Available exits include:

|User Exit|Description|
|---------|-----------|
|ZIGIXIT0 \(SAMPXIT0\)|Return the location of the Dovetail getpds and putpds commands if they are not found in the PATH.|

The exit driver is ZIGIEXIT, which is called passing the exit number:

Return = zigiexit\(\#\)

OR

Return = zigiexit\(\# data\)

The \# maps to the exit number \(for example: 0 to ZIGIXIT0\) and data is any information that the exit may require. Each exit returns the requested information.

*NEXT TOPIC*: [Appendix E: Common Problems](c_appendix_d_common_problems.md)

