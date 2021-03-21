        TITLE '*****  IGG026DU    CATALOG CONTROLLER 3 DUMMY MODULE'    00050060
IGG026DU CSECT                                                          00100060
**********************************************************************  00150060
*                                                                    *  00200060
*        MODULE NAME - IGG026DU                                      *  00250060
*                                                                    *  00300060
*        DESCRIPTIVE NAME - CATALOG CONTROLLER LEVEL 3 DUMMY MODULE  *  00350060
*                                                                    *  00400060
*        COPYRIGHT - NONE                                            *  00450060
*                                                                    *  00500060
*        STATUS - VS/2 RELEASE 3.7                                   *  00550060
*                                                                    *  00600060
*        FUNCTION                                                    *  00650060
*          THIS MODULE IS THE FIRST LOAD OF SVC 26 (CATALOG          *  00700060
*          MANAGEMENT). IT IS A DUMMY CSECT WHICH IMMEDIATELY PASSES *  00750060
*          CONTROL TO CATALOG MODULE IGC0002F WITHOUT CHANGING ANY   *  00800060
*          REGISTERS EXCEPT REGISTER 15.                             *  00850060
*                                                                    *  00900060
*          THIS CSECT MAY BE REPLACED BY A USER WRITTEN ROUTINE      *  00950060
*          IF DESIRED TO PERFORM PROCESSING BEFORE OR AFTER THE      *  01000060
*          SYSTEM CATALOG ROUTINES RECEIVE CONTROL.                  *  01050060
*                                                                    *  01100060
*          ANY USER WRITTEN ROUTINE WHICH REPLACES THIS CSECT MUST   *  01150060
*          BE RE-ENTRANT AND PASS CONTROL TO THE FIRST CATALOG       *  01200060
*          MODULE IGC0002F WITH THE REGISTER CONTENTS CONFORMING     *  01250060
*          TO STANDARD SVC ROUTINE CONVENTIONS. REGISTER 1 MUST      *  01300060
*          CONTAIN THE ADDRESS OF THE CATALOG PARAMETER LIST.        *  01350060
*                                                                    *  01400060
*          IF THE USER WRITTEN ROUTINE NEEDS TO SAVE REGISTERS,      *  01450060
*          IT MUST PROVIDE A RE-ENTRANT SAVE AREA TO SAVE AND        *  01500060
*          RESTORE ITS REGISTERS.  THE SVRB SAVE AREA SHOULD NOT     *  01550060
*          BE USED SINCE IT IS USED BY THE CATALOG ROUTINES.         *  01600060
*                                                                    *  01650060
*          DEPENDENCIES - EBCDIC CHARACTER CODE DEPENDENCIES - THIS  *  01700060
*                         MODULE MUST BE COMPILED AND EXECUTED ON    *  01750060
*                         A MACHINE WITH AN EBCDIC CHARACTER SET.    *  01800060
*                                                                       01850060
*                                                                    *  01900060
*          RESTRICTIONS - NONE                                       *  01950060
*                                                                    *  02000060
*          REGISTER CONVENTIONS -                                    *  02050060
*            UPON ENTRY TO IGG026DU:                                 *  02100060
*              R1 = CATALOG PARAMETER LIST ADDRESS                   *  02150060
*              R3 = POINTER TO CVT                                   *  02200060
*              R4 = POINTER TO TCB                                   *  02250060
*              R5 = POINTER TO SVRB                                  *  02300060
*             R14 = ADDRESS OF EXIT PROLOG                           *  02350060
*                                                                    *  02400060
*        MODULE TYPE - PROCEDURE                                     *  02450060
*                                                                    *  02500060
*          PROCESSOR - ASSEMBLER                                     *  02550060
*                                                                    *  02600060
*          MODULE SIZE - SEE LENGTH PRINTED IN EXTERNAL SYMBOL       *  02650060
*            DICTIONARY IN ASSEMBLY LISTING.                         *  02700060
*                                                                    *  02750060
*          ATTRIBUTES - REENTRANT AND READ-ONLY                      *  02800060
*                                                                    *  02850060
*        ENTRY POINT -                                               *  02900060
*          THE ONLY EXTERNAL ENTRY POINT OF THIS MODULE IS THE       *  02950060
*          MODULE NAME - IGG026DU. INVOKED BY SVC 26.                *  03000060
*                                                                    *  03050060
*          PURPOSE - TO ALLOW A USER WRITTEN ROUTINE TO BE EASILY    *  03100060
*                    PLACED BEFORE THE ENTRY POINT OF CATALOG.       *  03150060
*                                                                    *  03200060
*          LINKAGE - IGG026DU IS THE FIRST LOAD OF SVC 26 AND IS     *  03250060
*                    ENTERED VIA STANDARD LINKAGE CONVENTIONS        *  03300060
*                    WHENEVER SVC 26 IS INVOKED.                     *  03350060
*                                                                    *  03400060
*          INPUT -                                                   *  03450060
*            INPUT IS IN THE FORM OF A CATALOG REQUEST PARAMETER     *  03500060
*            LIST POINTED TO BY REGISTER 1.  THE LIST MAY BE IN THE  *  03550060
*            FORM OF AN OS/VS CAMLST OR A VSAM REQUEST LIST.         *  03600060
*                                                                    *  03650060
*          OUTPUT - REGISTER 15 CONTAINS THE ENTRY POINT ADDRESS OF  *  03700060
*            CATALOG MODULE IGC0002F. REGISTERS 0 - 14 ARE THE SAME  *  03750060
*            AS THEY WERE UPON ENTRY TO IGG026DU.                    *  03800060
*                                                                    *  03850060
*          EXIT NORMAL -                                             *  03900060
*            CONTROL IS PASSED TO THE CATALOG CONTROLLER MODULE      *  03950060
*            IGC0002F.                                               *  04000060
*                                                                    *  04050060
*          EXIT ERROR - NONE                                         *  04100060
*                                                                    *  04150060
*        EXTERNAL REFERENCES - NONE                                  *  04200060
*                                                                    *  04250060
*          DATA SETS - NONE                                          *  04300060
*                                                                    *  04350060
*          DATA AREAS - NONE                                         *  04400060
*                                                                    *  04450060
*        TABLES - NONE                                               *  04500060
*                                                                    *  04550060
*        MACROS - NONE                                               *  04600060
*                                                                    *  04650060
*        CHANGE ACTIVITY -                                           *  04700060
*                                                                    *  04750060
*    MODULE NEW FOR VS2-3.7  SU60                              @G60ASBJ 04800060
*                                                                    *  04850060
**********************************************************************  04900060
*REGISTER USAGE:                                                        04950060
R0       EQU   0                       REGISTER 0 - NOT CHANGED         05000060
R15      EQU   15                      BASE REGISTER - ENTRY POINT ADDR 05020060
         SPACE 3                                                        05040060
         BALR  R15,R0                  INITIALIZE REGISTER 15           05060060
         USING *,R15                   ESTABLISH BASE REGISTER          05080060
         L     R15,IGC0002F            GET ADDRESS OF IGC0002F ENTRY    05150060
         BR    R15                     TRANSFER CONTROL TO IGC0002F     05200060
IGC0002F DC    V(IGC0002F)             ENTRY POINT ADDRESS OF IGC0002F  05250060
         END                                                            05300060
