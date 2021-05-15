## Category

### What is `anaconda` in `conda create -n envname anaconda`?
- Metapackage, it collects together all the packages in the Anaconda installer.
- Install required packages automatically for `pykiwoom` (https://github.com/sharebook-kr/pykiwoom)
- https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/packages.html?highlight=metapackage#anaconda-metapackage
- https://www.anaconda.com/blog/whats-in-a-name-clarifying-the-anaconda-metapackage

### How do I setup `pykiwoom` environment?
- Open Anaconda Prompt and create 32-bit environment.
  - Why 32-bit? https://corytips.tistory.com/206
  - Why anaconda? https://lazyblue.tistory.com/9
```
(base) > set CONDA_FORCE_32BIT=1
(base) > conda create -n kiwoom python=3.7.9 anaconda
```
- Open Visual Studio Code with "관리자 권한으로 실행" and select `kiwoom` interpreter.
- Install `pykiwoom` (https://github.com/sharebook-kr/pykiwoom)
```
(kiwoom) > pip install -U pykiwoom
```
> :bangbang: **"AhnLab Safe Transaction" cause the error ("Python의 작동이 중지되었습니다.") whenever `pykiwoom` is terminated.** I wasted Sunday (2021-05-09) due to this issue. Refer to https://github.com/park9n/faq/blob/master/visual-studio-code.md#why-couldnt-i-find-terminal-select-default-shell-in-command-palette.

![Python의 작동이 중지되었습니다.](https://github.com/park9n/faq/blob/master/images/python.png)

### Where is `conda`'s default channel?
- Channels are locations where Navigator and conda look for packages: https://docs.anaconda.com/anaconda/navigator/tutorials/manage-channels/
- https://docs.anaconda.com/anaconda/user-guide/tasks/using-repositories/

### When can I use `pip` in a `conda` environment?
- https://www.anaconda.com/blog/using-pip-in-a-conda-environment
- https://docs.conda.io/projects/conda/en/master/user-guide/tasks/manage-environments.html#using-pip-in-an-environment

### How can I remove environment completely?
- https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#removing-an-environment
- https://stackoverflow.com/questions/58736579/conda-unable-to-completely-delete-environment
- https://github.com/conda/conda/issues/201

### Which version is selected if I use `conda create -n py37 python=3.7` instead of `conda create -n py37 python=3.7.9`?
- /// (Can't find answer)
