## Category

### How do I install Ubuntu 20.04.2 LTS?
- Select "Minimal installation" and install.
- (For VirtualBox full screen) `$ sudo apt-get install build-essential gcc make perl dkms`
- (For VirtualBox full screen) Reboot and install "VirtualBox Guest Additions".
- (For vim) `$ sudo apt install vim` and create `.vimrc`.
- (For git) `$ ssh-keygen -t ed25519 -C "your_email@example.com"` (https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) and add new SSH key to my GitHub account.
- (For git) `$ sudo apt install git-all` (https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) and configure `user.name`, `user.email`.
- (For venv) `$ sudo apt install python3-venv`
- (For venv) `$ python3 -m venv tutorial-env` (https://docs.python.org/3/tutorial/venv.html)
- (For venv) `$ source tutorial-env/bin/activate` (https://docs.python.org/3/tutorial/venv.html)

### How do I list files 'owned' by package(s)?
```
$ apt list --installed | grep "gtest"
$ dpkg-query -L libgtest-dev
```
- Also refer to https://askubuntu.com/questions/309113/what-is-the-difference-between-dpkg-and-aptitude-apt-get

### Where is desktop launcher (icon)?
`~/.local/share/applications/jetbrains-idea-ce.desktop`
- https://askubuntu.com/questions/537717/how-to-append-arguments-to-launch-an-application-with-specific-parameters-from-u

### How do I install Visual Studio Code?
- `$ sudo apt install ./<file>.deb` (https://code.visualstudio.com/docs/setup/linux#_debian-and-ubuntu-based-distributions)
- Execute: `$ code`

### What is POSIX?
- What is Linux? Unix? POSIX?: https://youtu.be/hy4OeVCLGZ4

### How do I change directories of `ls` from bold text to normal?
`LS_COLORS="di=00;34"`
- https://www.howtogeek.com/307899/how-to-change-the-colors-of-directories-and-files-in-the-ls-command/

### How do I enter Hangul?
- System Settings > Language Support
  - Language for menus and windows: 4 "English"s and "한국어"
  - Keyboard input method system: "IBus"

![image](https://user-images.githubusercontent.com/28881330/76437954-af786480-63fd-11ea-8681-748a60a581e9.png)

- System Settings > Text Entry > Add "Korean (Hangul) (IBus)"

![image](https://user-images.githubusercontent.com/28881330/76438572-80162780-63fe-11ea-9877-647d61938001.png)

- Change into Hangul: Ctrl+Space
- Toggle: Shift+Space
- https://selfish-developer.com/entry/%EC%9A%B0%EB%B6%84%ED%88%AC-1604-%ED%95%9C%EA%B8%80-%EC%9E%85%EB%A0%A5%ED%95%98%EA%B8%B0

### How do I install .deb?
`sudo apt install DEB_PACKAGE`
- https://unix.stackexchange.com/questions/159094/how-to-install-a-deb-file-by-dpkg-i-or-by-apt
- https://askubuntu.com/questions/40779/how-do-i-install-a-deb-file-via-the-command-line
- https://vitux.com/3-ways-to-install-software-from-deb-packages-in-ubuntu/

### How do I search previous commands?
`Ctrl+R` or `history`
- https://www.howtogeek.com/howto/44997/how-to-use-bash-history-to-improve-your-command-line-productivity/
- https://www.rootusers.com/17-bash-history-command-examples-in-linux/
- https://askubuntu.com/questions/1029850/why-is-history-and-bash-history-different-and-how-to-delete-an-entry-in-history

### How do I set `gedit` launcher as executing `gedit /home/cspark/note.txt`?
Modify `~/.local/share/applications/gedit.desktop` as below.
```
[Desktop Entry]
Encoding=UTF-8
Version=1.0
Type=Application
Name=gedit
Icon=gedit.png
Exec=gedit /home/cspark/note.txt
StartupNotify=false
StartupWMClass=Gedit
OnlyShowIn=Unity;
X-UnityGenerated=true
```
If you can't find `~/.local/share/applications/gedit.desktop` although you locked `gedit` to launcher, then copy `/usr/share/applications/org.gnome.gedit.desktop` into `~/.local/share/applications` and modify it as below (https://ubuntuforums.org/showthread.php?t=2359629).
```[Desktop Entry]
Name=gedit
GenericName=Text Editor
Comment=Edit text files
Exec=gedit /home/cspark/note.txt
Terminal=false
Type=Application
StartupNotify=true
MimeType=text/plain;
Icon=accessories-text-editor
Categories=GNOME;GTK;Utility;TextEditor;
X-GNOME-DocPath=gedit/gedit.xml
X-GNOME-FullName=Text Editor
X-GNOME-Bugzilla-Bugzilla=GNOME
X-GNOME-Bugzilla-Product=gedit
X-GNOME-Bugzilla-Component=general
X-GNOME-Bugzilla-Version=3.18.3
X-GNOME-Bugzilla-ExtraInfoScript=/usr/share/gedit/gedit-bugreport
Actions=new-window;new-document;
Keywords=Text;Editor;Plaintext;Write;
DBusActivatable=false
X-Ubuntu-Gettext-Domain=gedit

NoDisplay=true

[Desktop Action new-window]
Name=Open a New Window
Exec=gedit --new-window

[Desktop Action new-document]
Name=Open a New Document
Exec=gedit --new-document
```

### How do I see installed packages?
```
$ apt list --installed
$ apt list --installed "*chrome*"
```
https://www.cyberciti.biz/faq/apt-get-list-packages-are-installed-on-ubuntu-linux/

### How do I see file list of a package?
```
$ dpkg-query -L chromium-browser (for installed only)
or
$ apt-cache search "*chrome*"
$ dpkg --listfiles chromium-browser
```
https://askubuntu.com/questions/32507/how-do-i-get-a-list-of-installed-files-from-a-package

### What should I do if I entered Ctrl+S by mistake and the terminal freezed?
Type `Ctrl+Q`.
- https://unix.stackexchange.com/questions/12107/how-to-unfreeze-after-accidentally-pressing-ctrl-s-in-a-terminal
- https://www.networkworld.com/article/3438818/how-to-freeze-and-lock-your-linux-system-and-why-you-would-want-to.html

### What is `awk`, `sed` and `xargs`?
- `awk`: typically used as a data extraction and reporting tool. (https://en.wikipedia.org/wiki/AWK)
- `sed`: parses and transforms text. (https://en.wikipedia.org/wiki/Sed)
- `awk` vs. `sed`: Use sed for very simple text parsing. Anything beyond that, awk is better. (https://stackoverflow.com/questions/1632113/what-is-the-difference-between-sed-and-awk)
- `xargs`: converts input from standard input into arguments to a command. (https://en.wikipedia.org/wiki/Xargs)
