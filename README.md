# Notes

The dupe mod loads a jar called fabric-mixins.jar which is located inside the resource folder.

Fabric-mixins.jar loads a very long string from the "icon.png" file. I then decrypted that string (stage1.txt), which led me to stage2.txt, which is a obfuscated powershell script.

The channel has a lot of attention. One video has 60k views, which is concerning.

Thanks to firefish111 for decoding the main payload (https://github.com/firefish111)

# Stage 2

Stage 2 establishes a persistent communication channel with a remote server at https://193.34.77.163:8080. It collects system information (UUID, hostname, geolocation) and sends it to the server, retrieves Base64-encoded scripts, executes them as timed jobs, and logs the results back to the server. The script runs in an infinite loop, polling every 15 seconds for new commands, clears running jobs between cycles, and bypasses SSL certificate validation for HTTPS connections.


# IOCs

C2 Server: 193.34.77.163

Port: 8080

https://www.youtube.com/@JustMiloooo

https://www.youtube.com/watch?v=onWoYcSY_YM
