# ZGBATCH - Execute ZIGI in Batch

There may be projects where there is a need to schedule ZIGI to check for updated and new elements in a repository's z/OS data sets, which is where ZGBATCH is used.

The following is sample JCL:

```screen
//ZGBATCH JOB XXX,’ZIGI’,REGION=0M,NOTIFY=&SYSUID
//OUT   OUTPUT DEFAULT=YES,JESDS=ALL,OUTDISP=(HOLD,HOLD)
//* -------------------- *
//* INVOKE ISPF IN BATCH *
//* -------------------- *
//ISPF     EXEC PGM=IKJEFT1B,DYNAMNBR=50
//* -------------------------------- *
//* SYSEXEC IS WHERE THE CMD RESIDES *
//* -------------------------------- *
//SYSEXEC  DD  DISP=SHR,DSN=zigi.exec
//* ------------------------------- *
//* MLIB AND TLIB FOR THE REAL ISPF *
//* ------------------------------- *
//ISPMLIB  DD DISP=SHR,DSN=ISP.SISPMENU
//ISPTLIB DD  DISP=SHR,DSN=ISP.SISPTENU
//* ------------------------------------------------------ *
//* TEMPORARY PANELS, SKELETONS, AND TABLES ISPF LIBRARIES *
//* ALLOCATED TO VIO                                       *
//* ------------------------------------------------------ *
//ISPPLIB DD  DISP=(,DELETE),SPACE=(TRK,(1,1,1)),UNIT=VIO,
//            DCB=(RECFM=FB,LRECL=80,BLKSIZE=6160)
//ISPSLIB DD  DISP=(,DELETE),SPACE=(TRK,(1,1,1)),UNIT=VIO,
//            DCB=(RECFM=FB,LRECL=80,BLKSIZE=6160)
//ISPPROF DD  DISP=(,DELETE),SPACE=(TRK,(1,1,1)),UNIT=VIO,
//            DCB=(RECFM=FB,LRECL=80,BLKSIZE=6160)
//SYSTSPRT DD   SYSOUT=*
//* ----------------------------------------------- *
//* SYSTSIN - THE BATCH TSO COMMANDS TO INVOKE ISPF *
//* ----------------------------------------------- *
//SYSTSIN  DD   *
PROFILE PREFIX(userid)
ispf cmd(%zgbatch repo-prefix qualignr repo-directory P
/*
//COMMIT DD *     (Optional)
Commit subject line
Text line 1
Text line 2
/*

```

The zgbatch syntax is:

|Parameter|Description|
|---------|-----------|
|Repo-prefix|This is the ZIGI-defined z/OS prefix for the z/OS data sets within the repository.|
|Qualignr|The \# of qualifiers to ignore when constructing the OMVS filenames.|
|Repo-directory|The OMVS directory where the repository is located.|
|C or P|C to commit only or P to commit and push.|

*NEXT TOPIC:* [Timing \(For Those Interested\)](r_timing_for_those_interested.md)

