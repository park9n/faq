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
- https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-pkgs.html#installing-non-conda-packages

### How can I remove environment completely?
- https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#removing-an-environment
- https://stackoverflow.com/questions/58736579/conda-unable-to-completely-delete-environment
- https://github.com/conda/conda/issues/201

### Which version is selected if I use `conda create -n py37 python=3.7` instead of `conda create -n py37 python=3.7.9`?
- The latest patch (3.7.10 - refer to `conda search python`) is selected. If I use `conda create -n py38` without giving any **package_spec**, then empty environment will be created.
```
(base) C:\Users\cspark>conda create -n py37 python=3.7
Collecting package metadata (current_repodata.json): done
Solving environment: done


==> WARNING: A newer version of conda exists. <==
  current version: 4.9.2
  latest version: 4.10.1

Please update conda by running

    $ conda update -n base -c defaults conda



## Package Plan ##

  environment location: C:\Users\cspark\anaconda3\envs\py37

  added / updated specs:
    - python=3.7


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    certifi-2020.12.5          |   py37haa95532_0         141 KB
    pip-21.0.1                 |   py37haa95532_0         1.8 MB
    python-3.7.10              |       h6244533_0        14.5 MB
    setuptools-52.0.0          |   py37haa95532_0         711 KB
    wincertstore-0.2           |           py37_0          14 KB
    ------------------------------------------------------------
                                           Total:        17.1 MB

The following NEW packages will be INSTALLED:

  ca-certificates    pkgs/main/win-64::ca-certificates-2021.4.13-haa95532_1
  certifi            pkgs/main/win-64::certifi-2020.12.5-py37haa95532_0
  openssl            pkgs/main/win-64::openssl-1.1.1k-h2bbff1b_0
  pip                pkgs/main/win-64::pip-21.0.1-py37haa95532_0
  python             pkgs/main/win-64::python-3.7.10-h6244533_0
  setuptools         pkgs/main/win-64::setuptools-52.0.0-py37haa95532_0
  sqlite             pkgs/main/win-64::sqlite-3.35.4-h2bbff1b_0
  vc                 pkgs/main/win-64::vc-14.2-h21ff451_1
  vs2015_runtime     pkgs/main/win-64::vs2015_runtime-14.27.29016-h5e58377_2
  wheel              pkgs/main/noarch::wheel-0.36.2-pyhd3eb1b0_0
  wincertstore       pkgs/main/win-64::wincertstore-0.2-py37_0


Proceed ([y]/n)?
```
