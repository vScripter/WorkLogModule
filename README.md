<a name="Title">
# WorkLog Module


|Navigation|
|-----------------|
|[About](#About)|
|[Installation](#Installation)|
|[Examples](#Examples)|

<a name="About">
# About
[***Back to top***](#Title)

Module that contains functions that allow you to manage working with 'Work Log' markdown files

I created this module to quickly give me the ability to do basic file management for the markdown files I use for daily Work Logs, including getting the status/patch of the current Work Log file, creating a new Work Log file and adding new entries to the current Work Log file.

Functions include:
* ``Get-WorkLog``
* ``New-WorkLog``
* ``Add-WorkLog``

<a name="Installation"> 
# Installation
[***Back to top***](#Title)

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
  $ENV:PSModulePath -split ';'
  ```
  * Open PowerShell and run:
  ```powershell
  Import-Module WorkLog
  ```
  * Note: You may need to adjust your ExecutionPolicy
 
4. Make sure you update the $Path variables in each function. The default path location is:
  * ``$ENV:USERPROFILE\Documents\GitHub\WorkLog``

<a name="Examples"> 
# Examples
[***Back to top***](#Title)
### ``New-WorkLog``
  * ``New-WorkLog -Verbose``
  * ``New-WorkLog -Path $WorkFileWorkingDirectory -Verbose``
  
### ``Add-WorkLog``
```
Add-WorkLog 'This message will get added to the current Work Log file. If one does not exist, the file will be created'
```

You can use the ``-Indent`` parameter to support a hierarchy within your Work Log files
```
Add-WorkLog 'This message will indent one level, and appear as a bullet under the previous post' -Indent 1
```

Note: When using ``-Indent``, you may need to use ``Get-WorkLog`` if you don't remember what the current nesting level is.
 
### ``Get-WorkLog``
```
Get-WorkLog
```

This function uses ``Get-Content`` to display what the current Work Log file contents are, within the PowerShell console
  
  
