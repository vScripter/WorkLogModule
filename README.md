<a name="Title">
# WorkLog Module


|Navigation|
|-----------------|
|[About](#About)|
|[Installation](#Installation)|

<a name="About">
# About
Module that contains functions that allow you to manage working with 'Work Log' markdown files

I created this module to quickly give me the ability to do basic file management for the markdown files I use for daily Work Logs, including getting the status/patch of the current Work Log file, creating a new Work Log file and adding new entries to the current Work Log file.

Functions include:
* ``Get-WorkLog``
* ``New-WorkLog``
* ``Add-WorkLog``

<a name="Installation"> 
# Installation
1. Clone, Fork or download the .zip of the master source code
  * To download, you can copy/paste this into a PowerShell console, and it will download the module into your ``Downloads`` directory.
  ```powershell
(New-Object System.Net.WebClient).DownloadFile("https://github.com/vScripter/WorkLogModule/archive/master.zip","$ENV:USERPROFILE\Downloads\WorkLog.zip")
```

2. If you download the source:
  * Un-Block the .zip before un-zipping
  * Un-zip the source code

3. Move the 'WorkLog' directory into a valid PSModulePath directory
  * You can run the following, in PowerShell, to list valid directories:
  ```powershell
  ($ENV:PSModulePath).split(';')
  ```
  * Open PowerShell and run:
  ```powershell
  Import-Module ProcessIsolation
  ```
  * Note: You may need to adjust your ExecutionPolicy
