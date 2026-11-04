Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Install the latest PowerShell for new features and improvements! https://aka.ms/PSWindows

PS C:\Users\Workuser> & "C:\Program Files\mosquitto\mosquitto_sub.exe" -h localhost -p 1884 -t "com612/temperature" -m "22.5"
Error: Unknown option '-m'.

Use 'mosquitto_sub --help' to see usage.
PS C:\Users\Workuser> & "C:\Program Files\mosquitto\mosquitto_pub.exe" -h localhost -p 1884 -t "com612/temperature" -m "22.5"
PS C:\Users\Workuser> & "C:\Program Files\mosquitto\mosquitto_pub.exe" -h localhost -p 1884 -t "com612/temperature" -m "22.5"
PS C:\Users\Workuser> & "C:\Program Files\mosquitto\mosquitto_pub.exe" -h localhost -p 1884 -t "com612/temperature" -m "22.6"
PS C:\Users\Workuser> & "C:\Program Files\mosquitto\mosquitto_pub.exe" -h localhost -p 1884 -t "com612/temperature" -f .\sensor.json
Error: Unable to read file ".\sensor.json": No such file or directory.
Error loading input file ".\sensor.json".
PS C:\Users\Workuser> & "C:\Program Files\mosquitto\mosquitto_pub.exe" -h localhost -p 1884 -t "com612/temperature" -f .\sensor.json
Error: Unable to read file ".\sensor.json": No such file or directory.
Error loading input file ".\sensor.json".
PS C:\Users\Workuser> cd com612-mqtt
PS C:\Users\Workuser\com612-mqtt> & "C:\Program Files\mosquitto\mosquitto_pub.exe" -h localhost -p 1884 -t "com612/temperature" -f .\sensor.json
PS C:\Users\Workuser\com612-mqtt> & "C:\Program Files\mosquitto\mosquitto_pub.exe" -h localhost -p 1884 -t "com612/humidity" -m "48"
PS C:\Users\Workuser\com612-mqtt> & "C:\Program Files\mosquitto\mosquitto_pub.exe" -h localhost -p 1884 -t "com612/humidity" -m "30"
PS C:\Users\Workuser\com612-mqtt> & "C:\Program Files\mosquitto\mosquitto_pub.exe" -h localhost -p 1884 -t "com612/humidity" -m "30"^C






Install the latest PowerShell for new features and improvements! https://aka.ms/PSWindows

PS C:\Users\Workuser> & "C:\Program Files\mosquitto\mosquitto_sub.exe" -h localhost -p 1884 -t "com612/temperature" -v
com612/temperature 22.5
com612/temperature 22.5
com612/temperature 22.6
com612/temperature {"sensor": "NTC" , "temperature" :23.4, "unit":"c"}
PS C:\Users\Workuser> & "C:\Program Files\mosquitto\mosquitto_sub.exe" -h localhost -p 1884 -t "com612/#" -v
com612/humidity 48
com612/humidity 30
