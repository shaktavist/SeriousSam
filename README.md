# SeriousSam
Windows Elevation of Privilege Vulnerability CVE-2021-36934

Description see MS article: https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-36934

To deploy the workaround via GPO

Copy paste the below commands in notepad, save as a batch file (.bat extension) and then use to push on to windows machines via GPO.

**@echo off
icacls %windir%\system32\config\*.* /inheritance:e
vssadmin delete shadows /all /quiet**

As always advise is to test this first prior to mass deployment.

