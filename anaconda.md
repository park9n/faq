## Category

### What is `anaconda` in `conda create -n envname anaconda`?
- Metapackage, it collects together all the packages in the Anaconda installer.
- Install required packages automatically for `pykiwoom` (https://github.com/sharebook-kr/pykiwoom)
- https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/packages.html?highlight=metapackage#anaconda-metapackage
- https://www.anaconda.com/blog/whats-in-a-name-clarifying-the-anaconda-metapackage

### How do I setup `pykiwoom` environment?
- Open Anaconda Prompt with "관리자 권한으로 실행"
- Create 32-bit environment.
  - Why 32-bit? https://corytips.tistory.com/206
  - Why anaconda? https://lazyblue.tistory.com/9
```
(base) $ set CONDA_FORCE_32BIT=1
(base) $ conda create -n kiwoom python=3.7.9 anaconda
```
- Open Visual Studio Code with "관리자 권한으로 실행" and select environment.
- Install `pykiwoom` (https://github.com/sharebook-kr/pykiwoom)
```
(kiwoom) $ pip install -U pykiwoom
```