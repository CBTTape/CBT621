# CBT621
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)
This is still a work in progress. GitHub repos will be deleted and created during this period...
~~~~~~~~~~~~~~~~

//***FILE 621 is from Hunter Zhou, and contains some TCP/IP NPF     *   FILE 621
//*           Exit Programs to print mainframe datasets directly    *   FILE 621
//*           to any network printer with PCL language support.     *   FILE 621
//*           Most laser printers support PCL, such as HP,          *   FILE 621
//*           Xerox, Canon, Lexmark.  The program will also         *   FILE 621
//*           generate a banner page to identify the sender.        *   FILE 621
//*                                                                 *   FILE 621
//*     Package Name: NPF Input Record Exit Programs for            *   FILE 621
//*                   network printers                              *   FILE 621
//*     Design      : Hunter Guanghui Zhou                          *   FILE 621
//*                   Phone: 1-(416)-602-9567                       *   FILE 621
//*                   E-mail: zhough2000@yahoo.com                  *   FILE 621
//*     Date        : September 2003                                *   FILE 621
//*                                                                 *   FILE 621
//*     Package Description                                         *   FILE 621
//*     -------------------                                         *   FILE 621
//*      TCP/IP NPF(Network Print Facility) is a free feature       *   FILE 621
//*      of OS/390 and z/OS. It can print JES and VTAM data to      *   FILE 621
//*      network printers via TCP/IP printer servers(LPD            *   FILE 621
//*      servers).                                                  *   FILE 621
//*                                                                 *   FILE 621
//*      NPF provides three different exit interfaces. Here I       *   FILE 621
//*      created one of them: Input Record Exit. The Input          *   FILE 621
//*      Record Exit is used to insert a banner page, update        *   FILE 621
//*      the input record.                                          *   FILE 621
//*                                                                 *   FILE 621
//*      Normallly, NPF uses LPR program to send data to remote     *   FILE 621
//*      printer servers. However, for those printer without        *   FILE 621
//*      Postscript support features, you cannot print your         *   FILE 621
//*      data sets in landscape via LPR.                            *   FILE 621
//*                                                                 *   FILE 621
//*      This package extends the capability of NPF with            *   FILE 621
//*      following features:                                        *   FILE 621
//*                                                                 *   FILE 621
//*        .Pure TCP/IP, not require SNA gateway                    *   FILE 621
//*        .Send data directly from Mainframe to network            *   FILE 621
//*         printers                                                *   FILE 621
//*        .Insert PCL commands to control the printer              *   FILE 621
//*         settings.                                               *   FILE 621
//*        .Support duplex print out (if the printers support).     *   FILE 621
//*        .Support following Carriage Control data:                *   FILE 621
//*           .ASA Carriage Control Commands                        *   FILE 621
//*           .Printer Channel Commands (Machine Code)              *   FILE 621
//*        .Provide banner page to identify the printer out.        *   FILE 621
//*                                                                 *   FILE 621
//*      Here I included 8 exit programs generated by single        *   FILE 621
//*      assembler source in single JCL. The options are given      *   FILE 621
//*      via Compiler EXEC SYSPARM.                                 *   FILE 621
//*                                                                 *   FILE 621
//*  EXIT     Printer Type        Orientation PAPER   CC  Duplex    *   FILE 621
//*  ======== =================== =========== ======= === ======    *   FILE 621
//*  EXPCLLG0 IP Printer w/ PCL 5  LANDSCAPE  Legal   Yes Yes       *   FILE 621
//*  EXPCLLG1 IP Printer w/ PCL 5  PORTRAIT   Legal   No  Yes       *   FILE 621
//*  EXPCLLS0 IP Printer w/ PCL 5  LANDSCAPE  Default Yes Yes       *   FILE 621
//*  EXPCLLS1 IP Printer w/ PCL 5  LANDSCAPE  Default No  Yes       *   FILE 621
//*  EXPCLPT0 IP Printer w/ PCL 5  PORTRAIT   Default Yes Yes       *   FILE 621
//*  EXPCLPT1 IP Printer w/ PCL 5  PORTRAIT   Default No  Yes       *   FILE 621
//*  EXTEXT00 IP Printer w/ TEXT   DEFAULT    Default No  No        *   FILE 621
//*  EXTEXT01 IP Printer w/ TEXT   DEFAULT    Default Yes No        *   FILE 621
//*                                                                 *   FILE 621
//*      EXTEXT01 sends text file (translated any CC to ASCII       *   FILE 621
//*      control codes) to network text printers. You can use       *   FILE 621
//*      it to send print data to network impact printers, such     *   FILE 621
//*      as Printronix P5000.                                       *   FILE 621
//*                                                                 *   FILE 621
~~~~~~~~~~~~~~~~
