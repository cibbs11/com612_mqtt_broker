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





PS C:\Users\Workuser> & "C:\Program Files\mosquitto\mosquitto.exe" -c "c:\users\workuser\COM612-MQTT\mosquitto-local.conf" -v
1793807462: mosquitto version 2.1.2 starting
1793807462: Config loaded from c:\users\workuser\COM612-MQTT\mosquitto-local.conf.
1793807462: Bridge support available.
1793807462: Persistence support available.
1793807462: TLS support available.
1793807462: TLS-PSK support available.
1793807462: Websockets support available.
1793807462: Opening ipv4 listen socket on port 1884.
1793807462: mosquitto version 2.1.2 running
1793807586: New connection from 127.0.0.1:25384 on port 1884.
1793807586: New client connected from 127.0.0.1:25384 as auto-BB256850-6288-2014-A254-D4E29688BEC5 (p4, c1, k60).
1793807586: No will message specified.
1793807586: Sending CONNACK to auto-BB256850-6288-2014-A254-D4E29688BEC5 (0, 0)
1793807586: Received SUBSCRIBE from auto-BB256850-6288-2014-A254-D4E29688BEC5
1793807586:     com612/temperature (QoS 0)
1793807586: auto-BB256850-6288-2014-A254-D4E29688BEC5 0 com612/temperature
1793807586: Sending SUBACK to auto-BB256850-6288-2014-A254-D4E29688BEC5
1793807643: New connection from 127.0.0.1:25450 on port 1884.
1793807643: New client connected from 127.0.0.1:25450 as auto-3B6E11A2-ECBD-7341-C7C7-0982E65B02DC (p4, c1, k60).
1793807643: No will message specified.
1793807643: Sending CONNACK to auto-3B6E11A2-ECBD-7341-C7C7-0982E65B02DC (0, 0)
1793807643: Received PUBLISH from auto-3B6E11A2-ECBD-7341-C7C7-0982E65B02DC (d0, q0, r0, m0, 'com612/temperature', ... (4 bytes))
