## Category

### Can I build using existing Makefile in Code?
- https://devblogs.microsoft.com/cppblog/building-your-c-application-with-visual-studio-code/
- https://code.visualstudio.com/docs/getstarted/introvideos

### How can I debug?
TBD

### Can I use formatter?
- https://code.visualstudio.com/docs/editor/codebasics#_formatting
- Change style: https://stackoverflow.com/questions/45823734/vs-code-formatting-for

### How do I setup for Python?
- https://code.visualstudio.com/docs/python/python-tutorial
- Open Folder → New Terminal (`python -m venv .venv`) → New File (`hello.py`) → Install Python extension (Interpreter is updated to `.venv`) → Run Python File in Terminal

### Why couldn't I find "Terminal: Select Default Shell" in Command Palette?
- Changed to "Terminal: Select Default Profile" from 1.56 (https://code.visualstudio.com/updates/v1_56#_terminal). However this update reproduce old syntax error (https://stackoverflow.com/questions/56456924/ampersand-syntax-error-running-any-python-script-in-vscode) by adding "&" to the head of commands. Unfortunately I downloaded 1.56 and wasted Saturday (2021-05-08) due to this issue. Simply use 1.55 (https://code.visualstudio.com/updates/v1_55) until fixed.
