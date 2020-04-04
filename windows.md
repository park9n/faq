## Category

### How do I change "네트워크2" into "네트워크"?
1. Win + R (실행) > regedit
1. Go to `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\NetworkList\Profiles`
1. Remove unused profiles and change "네트워크2"'s `ProfileName`.
