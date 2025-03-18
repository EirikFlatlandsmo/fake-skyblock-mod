# Investigation

The dupe mod loads a jar called fabric-mixins.jar which is located inside the resource folder.

Fabric-mixins.jar loads a very long string from the "icon.png" file. I then decrypted that string (stage1.txt), which led me to stage2.txt, which is a obfuscated powershell script.
