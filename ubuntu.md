**Q. How do I list files 'owned' by package(s)?**
```
$ apt list --installed | grep "gtest"
$ dpkg-query -L libgtest-dev
```
- Also refer to https://askubuntu.com/questions/309113/what-is-the-difference-between-dpkg-and-aptitude-apt-get

**Q. Where is desktop launcher (icon)?**

`~/.local/share/applications/jetbrains-idea-ce.desktop`
