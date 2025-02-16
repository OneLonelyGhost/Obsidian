## local admin

`$pass =` [password](https://dunedinit.eu.itglue.com/1024763/passwords/folder/1608027073806591)
`net user itsupport $pass | net localgroup administrators itsupport /add`

.\itsupport
[password](https://dunedinit.eu.itglue.com/1024763/passwords/folder/1608027073806591)

wmic 
useraccount where name='it support' rename itsupport

powercfg command to stop lid close causing poweroff
----------------------------------------------------

`powercfg -SETDCVALUEINDEX 381b4222-f694-41f0-9685-ff5bb260df2e 4f971e89-eebd-4455-a8de-9e59040e73475ca83367-6e45-459f-a27b-476b1d01c936 3`

`powercfg -SETACVALUEINDEX 381b4222-f694-41f0-9685-ff5bb260df2e 4f971e89-eebd-4455-a8de-9e59040e73475ca83367-6e45-459f-a27b-476b1d01c936 3`

sage autoupdate prevent
-----------------------
`sc stop "Sage AutoUpdate Manager Service" && sc config "Sage AutoUpdate Manager Service" start=disabled`

`sc stop "Sage AutoUpdate Manager Service v2" && sc config "Sage AutoUpdate Manager Service v2" start=disabled`

device manager
-----------------
*win+r*
devmgmt.msc

system properties
-----------------
*win+r*
sysdm.cpl

bypass 365 account set up
------------------------
*shft+fn+f10*
oobe\bypassnro

oobe re-image
--------------
*win+r*
%WINDIR%\system32\sysprep\sysprep.exe

clear new outlook
-------------------
*win+r*
olk.exe --clearLocalState


RENAME pc
-----------
`Rename-Computer -NewName "" -DomainCredential Domain01\Admin01 -Restart`
`Rename-Computer -NewName "" -Restart`


speccy
--------
`winget install --id=Piriform.Speccy -e`
`winget uninstall --id=Piriform.Speccy -e`

incident tickets
----------------
general user
securitynotifications@dunedinit.co.uk