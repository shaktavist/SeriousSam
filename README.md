<p><strong>Windows Elevation of Privilege Vulnerability CVE-2021-36934&nbsp; &nbsp;#SeriousSAM</strong></p>
<p>Description see MS article:&nbsp;<a href="https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-36934">https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-36934</a></p>
<p>&nbsp;</p>
<p><strong><u>To deploy the workaround via GPO</u></strong></p>
<p>Copy paste the below commands in notepad, save as a batch file (.bat extension) and then use to push on to windows machines via GPO.</p>
<p><strong><em>@echo off icacls %windir%\system32\config*.&nbsp;/inheritance:e</em></strong></p>
<p><strong><em>vssadmin delete shadows /all /quiet</em></strong><strong>*</strong></p>
<p>As always, I would advise to test this first prior to mass deployment.</p>
