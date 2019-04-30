Change Log
==========

![](http://i.imgur.com/5yZfZi5.jpg)


CIS-CAT Pro Assessor v4
---------------------------
See the CIS-CAT Pro Assessor Coverage Guide for information about supported benchmarks, OVAL schemas/test types, and scripting capabilities.

## CIS-CAT Pro Assessor, v4.0.5 ##
#### Release Date: April 30, 2019 ####


### New Benchmarks ###
- None

### Benchmark Updates ###
- CIS Microsoft Windows 10 Enterprise 1803 v1.5.0.1 - scoring modification only for profile selection of ‘Windows 10 1803 Level 1 (L1) + BitLocker (BL) + Next Generation Windows Security (NG)’ or 'Windows 10 1803 Level 1 (L1) + BitLocker (BL)'

### CIS-CAT Pro Updates ###
-  Cisco IOS assessments will now produce accurate results when performing local and remote assessments.
-  Number only credentials for endpoints utilized in the configuration xml files are now valid.
-  A broader explanation and more generic referral to Level 1 Windows Benchmark recommendations that require consideration when remote scanning has been added to the online documentation. In order to remotely scan, users may need to except 2 or more recommendations.
-  Online documentation has been revised for Windows Endpoint Configuration to be more specific to users' environments.

## CIS-CAT Pro Assessor, v4.0.4 ##
#### Release Date: March 20, 2019 ####


### New Benchmarks ###
- CIS MS Windows 10 Enterprise Release 1803 Benchmark v1.5.0. Updates to centralized scripts and dissolvable bundle to accommodate the new Benchmark. CIS-CAT Pro will support the latest three published Windows Enterprise Benchmarks.
- CIS PostgreSQL 9.6 v1.0.0

### Benchmark Updates ###
- CIS Amazon Linux 2 v1.0.0.1 with updated Controls 7 mapping only
- CIS Microsoft IIS 10 Benchmark v1.1.1
- CIS PostgreSQL 9.5 v1.1.0.1

### CIS-CAT Pro Updates ###
-  Configuration XML files and sessions.properties files used to drive the assessment process can be encrypted.  See the **"File Encryption Options"** section of the User's Guide for more information.
-  Scripts are included for Linux and Windows environments to scan an entire domain when target machines have access to a network Java instance and CIS-CAT Pro Assessor. This is useful for members who want to use the assessor within a domain instead of remotely connecting to each target. See the **"Assessing Multiple Windows Targets"** and **"Assessing Multiple Unix/Linux Targets"** sections of the User's Guide for more information.
-  On screen message for local assessments will let users know if they lack privileges to execute the assessment.
-  The connection to remote endpoints has been modified to be more efficient.
-  Enhanced documentation with information on allowed characters used within the configuration XML file.
-  Linux configuration results have been corrected for reported issues on Linux CentOS recommendation 6.2.6.

## CIS-CAT Pro Assessor, v4.0.3 ##
#### Release Date: January 17, 2019 ####


### New Benchmarks ###
- CIS Debian Linux 9 Benchmark v1.0.0

### Benchmark Updates ###
- CIS Debian Linux 8 Benchmark v2.0.0
- CIS Microsoft IIS 10 Benchamrk v1.1.0
- CIS PostgreSQL 9.5 Benchmark v1.1.0

### CIS-CAT Pro Updates ###
-  Assessment result HTML reports now show the CIS Controls and CIS Sub-control version numbers when mapped to a CIS Benchmark recommendation. The CIS Control version is only available on some Benchmarks. Check the CIS website for more information. The title page of the report has also been enhanced to display long Benchmark names.
-  Scripts have been modified to allow an assessment to execute with OpenJDK, Java 9, Java 10, and Java 11.
-  User's Guide updated in section titled "Using CIS-CAT Pro Assessor CLI" to highlight requirement for a the user executing the application to have root, Administrator, or an equivalently privileged principal.
-  CIS-CAT Pro assessor has been enhanced to more efficiently work with OVAL content that uses XPath.
-  CIS Microsoft IIS 10 Benchmark has been corrected to properly collect assessment information. In prior versions, some users may have experienced false failures.
-  An issue was resolved with interactive values when users configured private keys with passphrases. The command line will now prompt users to enter a passphrase when the passphrase element is present and null in the Sessions or Config file. If the passphrase element does not exist for a target in the sessions or configuration xml, the command line will not prompt the user for an entry.
-  Report generation errors have been resolved for all versions of CIS Apple OSX 10.10, 10.11 and 10.12 Benchmark.    

## CIS-CAT Pro Assessor, v4.0.2 ##
#### Release Date: November 28, 2018 ####


### New Benchmarks ###
- None

### Benchmark Updates ###
- None

### CIS-CAT Pro Updates ###
-  Resolved User_object NPE/fatal error that occurs during some assessments.
-  Assessment results produced in csv format will now be modified per options set using the -D option.

## CIS-CAT Pro Assessor, v4.0.1 ##
#### Release Date: November 21, 2018 ####


### New Benchmarks ###
- CIS Amazon Linux 2 Benchmark v1.0.0

### Benchmark Updates ###
- CIS Benchmark for Windows Server 2016, v1.1.0

### CIS-CAT Pro Updates ###
-  Assessor-CLI.sh invalid Windows escape characters, preventing immediate run on Linux, have been removed.
-  ARF and OVAL vulnerability XML reports are now UTF-8 encoded to prevent invalid, non-UTF-8 characters from appearing in the report. The presence of these characters, can cause a problem when importing reports into other applications such as CIS-CAT Pro Dashboard.
- The environment command has been enhanced to handle variables configured over multiple lines.
- The ability to disable/enable schema validation now functions when configured in the assessor-cli.properties file.
- The creation of the Linux file item will no longer fail when a file size result is longer than maximum integer size.
- An update was made to the linux file collection process to account for the "xsi:nil=true" value in the filename element.

## CIS-CAT Pro Assessor, v4.0.0 ##
#### Release Date: October 26, 2018 ####
This is the initial release of CIS-CAT Pro Assessor v4 (CCPA), a command-line user interface enabling configuration and vulnerability assessment of endpoints.

### Assessor Updates ###
- Assessment of the system from which the Assessor is invoked.  This functionality mimics the host-based assessments from CIS-CAT v3.
- Assessment of remote Windows endpoints using WinRM and an "ephemeral" agent.
- Assessment of remote Unix/Linux endpoints using an SSH-based connection.
- Assessment of Cisco IOS network devices using an SSH-based connection.
- Support for the assessment of Security Content Automation Protocol (SCAP) 1.2 data-stream collections.
- Support for the assessment of XCCDF 1.2-based content.
- Support for the assessment of OVAL Definitions files, such as inventory and vulnerability definitions.
- Support for multiple report formats, such as the Asset Reporting Format and OVAL Results with System Characteristics in XML format, as well as HTML, CSV, or plain-text formats.
- Support for the upload of assessment results to CIS-CAT Pro Dashboard.