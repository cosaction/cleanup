# Cleanup

A set of browser automation macros to be used with the UI.Vision Kantu browser extension https://ui.vision/.

Questions can be directed to aaycock@cosaction.com.

Recommended Extension Settings:

![Recommended extension settings](recommendedExtensionSettings.png)


Notes on the RunCleanupForever.ps1 PowerShell script:
* To be able to execute (WIN 10 Home v. 2004 ), override default WIN PowerShell execution setting as it is "Restricted" by default.  For testing, set "Bypass" for the current PowerShell session:  `Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope process`
* Currently configured to use Chrome browser: `$cmd = "${env:ProgramFiles(x86)}\Google\Chrome\Application\chrome.exe"`.   
* Hardcoded chrome path for testing.  Both PowerShell 32 & 64 bit exist but regardless of which is used commands *${env:ProgramFiles}* and *${env:ProgramFiles(x86)}* both return 'Program Files (x86)', and Chrome 64 bit is installed in 'Program Files'.  `$cmd = "C:\Program Files\Google\Chrome\Application\chrome.exe"`
* Hardcoded path in use: `$path_downloaddir = "C:\Users\troy.day\Downloads\" `
* Test in QA environment by replacing all occurances of conventionofstates.com with qacos.com in these files: 
  * COS Clean Up (Play me!).json:  
  * COS People address.json:
  * COS Petition email_errors.json:
  * COS Petition need_review.json:
  * COS Voter Voice.json:
  * COS melissa_search.json:

