# gspromenuchanger
GSPro Menu Music Changer
This scheduled task will run as often as you choose through a task scheduler built into Windows.  To use, follow these steps:
1: Download the RandomMusic code, open it in notepad, copy its contents and paste in to powershell ise
2: On your PC create a folder for the music, it has to be a .wav file, wherever you created that folder, and whatever you name it, put that path in the script on line 3 for $menuMusicFolder = "your/path/here"
3: Place the .wav files you have in the folder you created
4: Create a scheduled task by opening Task Scheduler and clicking Create Task.  Name the task whatever you want.  Under the Triggers tab, create new and set the time you want the script to run.  For example mine runs once daily.  You can set it to run daily, then under advanced settings you can have it repeat during the day however often you'd like.  Under the Actions tab, click new, for action choose start a program, paste the following in Program/script:  C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe        In the add arguments field paste the following: -ExecutionPolicy Bypass -File "your\script\path\here.ps1"  
Afterwards you can click OK as the other tabs are typically left blank.  From there you can run the task and make sure the files in your music folder change names and that the music inside of GSPro upon boot is changing.
