## Hi there 👋

<!--
**eliwiz/eliwiz** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
# Look for ANY interesting strings in the "no results" binaries
strings.exe -accepteula "C:\Users\nuccdc\AppData\Local\Temp\{1AB8CB13-F1A2-4248-B31F-0D2C6CF0612A}\idle.exe" > idle_all_strings.txt

strings.exe -accepteula "C:\Users\nuccdc\AppData\Local\Programs\Python\Python311\tcl\nmake\x86_64-w64-mingw32-nmakehip.exe" > nmakehip_all_strings.txt

strings.exe -accepteula "C:\Users\nuccdc\AppData\Local\Temp\{54724SC6-4AA5-4DF9-856A-623D174A9B02}-MicrosoftEdgeUpdateSetup_X86_1.3.203.13.exe" > edge_all_strings.txt

# More flexible IP search
strings.exe -accepteula "idle.exe" | findstr /r "[0-9][0-9]*\.[0-9][0-9]*\.[0-9][0-9]*\.[0-9][0-9]*"

# Check if files are digitally signed
sigcheck.exe -accepteula "idle.exe"
sigcheck.exe -accepteula "nmakehip.exe"
