https://www.skillrary.com/blogs/read/malware

https://www.skillrary.com/blogs/read/basics-of-cryptography

https://www.skillrary.com/blogs/read/top-cybersecurity-certification-which-can-fetch-you-a-job-for-life

# cybersecurity
Hands on Materials for Cyber Security Course

Install latest Python from python.org

pip install pywin32

pip install pynput

shutdown.exe -s -t 30 -c owned

1) Keyboard lights trick (.vbs)

Set wshShell =wscript.CreateObject("WScript.Shell")
do
wscript.sleep 100
wshshell.sendkeys "{CAPSLOCK}"
wshshell.sendkeys "{NUMLOCK}"
wshshell.sendkeys "{SCROLLLOCK}"
loop

2) Optical disc drive trick (.vbs)

Set oWMP = CreateObject("WMPlayer.OCX.7")
Set colCDROMs = oWMP.cdromCollection
do
if colCDROMs.Count >= 1 then
For i = 0 to colCDROMs.Count -1
colCDROMs.Item(i).Eject
Next
For i = 0 to colCDROMs.Count -1
colCDROMs.Item(i).Eject
Next
End If
wscript.sleep 5000
loop

3) Fake error message (.vbs)

x=msgbox("Your Message Here", 0+16, "Your Title Here")

4) Matrix code - type 1 (.bat)

@echo off
color 02
:start
echo %random% %random% %random% %random% %random% %random% %random% %random% %random% %random%
goto start

5) Matrix code - type 2 (.bat)

@echo off
:a
color 2
echo 1 1 1 0 1 0 0 0 1 1 1 1 0 0 0 1 1 0 0 1 0 0 0 1 1 0 1 0 1 0 0 0 1 1 1 1
ping localhost -n 1 > nul
echo 1 1 0 1 1 1 0 0 0 1 0 1 a f h 0 0 0 1 0 1 1 0 0 1 1 1 0 0 1 0 1 0 0 1 1 0
echo 1 0 0 1 1 0 9 8 1 2 0 1 9 9 2 1 1 1 0 0 1 0 1 1 1 0 1 1 0 1 0 0 0 1 0 1 1
ping localhost -n 1 > nul
echo 0 1 0 0 0 1 0 0 0 1 0 0 0 1 0 1 0 0 1 0 1 0 1 1 0 1 0 0 0 01 0 1 0 0 1 0
ping localhost -n 1 > nul
echo 1 0 1 1 1 0 1 1 0 9 1 1 2 1 1 0 9 1 0 5 7 7 8 7 8 1 3 2 1 2 1 2 3 2 1 3 4
ping localhost -n 1 > nul
echo 1 1 1 0 1 0 0 1 0 0 0 1 1 1 0 0 1 1 1 4 1 2 1 1 2 0 1 0 1 2 2 1 0 1 1 0 1
goto a

6) Notepad diary (no special extension is required)

.LOG

7) Guessing game (.bat)

@echo off
color 0e
title Guessing Game by seJma
set /a guessnum=0
set /a answer=%RANDOM%
set variable1=surf33
echo -------------------------------------------------
echo Welcome to the Guessing Game! 
echo. 
echo Try and Guess my Number! 
echo -------------------------------------------------
echo. 
:top
echo. 
set /p guess=
echo. 
if %guess% GTR %answer% ECHO Lower! 
if %guess% LSS %answer% ECHO Higher! 
if %guess%==%answer% GOTO EQUAL
set /a guessnum=%guessnum% +1
if %guess%==%variable1% ECHO Found the backdoor hey?, the answer is: %answer%
goto top
:equal
echo Congratulations, You guessed right!!! 
echo. 
echo It took you %guessnum% guesses. 
echo. 
pause

8) Password generator (.bat)

@echo off
:Start2
cls
goto Start
:Start
title Password Generator
echo I will make you a new password. 
echo Please write the password down somewhere in case you forget it. 
echo ----------------------------------------¬-----------------------
echo 1) 1 Random Password
echo 2) 5 Random Passwords
echo 3) 10 Random Passwords
echo Input your choice
set input=
set /p input= Choice: 
if %input%==1 goto A if NOT goto Start2
if %input%==2 goto B if NOT goto Start2
if %input%==3 goto C if NOT goto Start2
:A
cls
echo Your password is %random%
echo Now choose what you want to do. 
echo 1) Go back to the beginning
echo 2) Exit
set input=
set /p input= Choice: 
if %input%==1 goto Start2 if NOT goto Start 2
if %input%==2 goto Exit if NOT goto Start 2
:Exit
exit
:B
cls
echo Your 5 passwords are %random%, %random%, %random%, %random%, %random%.
echo Now choose what you want to do. 
echo 1) Go back to the beginning
echo 2) Exit
set input=
set /p input= Choice: 
if %input%==1 goto Start2 if NOT goto Start 2
if %input%==2 goto Exit if NOT goto Start 2
:C
cls
echo Your 10 Passwords are %random%, %random%, %random%, %random%, %random%, %random%, %random%, %random%, %random%, %random%
echo Now choose what you want to do. 
echo 1) Go back to the beginning
echo 2) Exit
set input=
set /p input= Choice: 
if %input%==1 goto Start2 if NOT goto Start 2
if %input%==2 goto Exit if NOT goto Start 2

9) Private folder (.bat)

Quote:
Quote: cls
@ECHO OFF
title Folder Private
if EXIST "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" goto UNLOCK
if NOT EXIST Private goto MDLOCKER
:CONFIRM
echo Are you sure you want to lock the folder(Y/N)
set/p "cho=>"
if %cho%==Y goto LOCK
if %cho%==y goto LOCK
if %cho%==n goto END
if %cho%==N goto END
echo Invalid choice.
goto CONFIRM
:LOCK
ren Private "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
attrib +h +s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
echo Folder locked
goto End
:UNLOCK
echo Enter password to unlock folder
set/p "pass=>"
if NOT %pass%== password goto FAIL
attrib -h -s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"
ren "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" Private
echo Folder Unlocked successfully
goto End
:FAIL
echo Invalid password
goto end
:MDLOCKER
md Private
echo Private created successfully
goto End
:End

10) Text to speech (.vbs)

Dim message, sapi
message=InputBox("What do you want me to say?","Speak to Me")
Set sapi=CreateObject("sapi.spvoice")
sapi.Speak message

11) Shutdown computer with custom message (.bat)

@echo off
Shutdown.exe -s -t 10
cls
msg * your message here!



References from the class:

https://cybersecurityventures.com/hackerpocalypse-cybercrime-report-2016/

https://cybersecurityventures.com/cybercrime-damages-6-trillion-by-2021/

https://www.mailguard.com.au/blog/fbi-fraud-1-cybercrime

https://www.forbes.com/sites/gilpress/2018/12/03/60-cybersecurity-predictions-for-2019/#3e16438f4352

https://www.forbes.com/sites/gradsoflife/2019/03/19/the-1-mentality-how-it-can-close-the-gender-and-race-gap/#29d0894c3474

https://www.gartner.com/en/information-technology/insights/cybersecurity

https://en.wikipedia.org/wiki/Yahoo!_data_breaches

https://us.norton.com/internetsecurity-emerging-threats-10-facts-about-todays-cybersecurity-landscape-that-you-should-know.html

https://outpost24.com/blog/top-10-of-the-world-biggest-cyberattacks

https://www.arnnet.com.au/slideshow/341113/top-10-most-notorious-cyber-attacks-history/
