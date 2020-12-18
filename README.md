# tornado_startup_script
This repo contains a sample windows script as a bat file to launch a tornado app on startup.

We will create a bat file, that when double clicked it will launch your tornado app, and then we will palce this bat file in a given windows folder so when the machine it is started, the script is executed. 

If you are targetting a specific python version that is not in the PATH environmen variable, you can modify the following

python ./app.py

to

C:\tools\python36\python.exe ./app.py

To launch the script, create a task with the following command (for this you will need admin rights):

schtasks.exe /create /tn "Tornado App Server" /ru SYSTEM /Sc ONSTART /tr
"C:\tornado_startup.bat"
