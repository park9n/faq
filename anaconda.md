## Category

### What is `anaconda` in `conda create -n envname anaconda`?
- Metapackage, it collects together all the packages in the Anaconda installer.
- Useful to use https://github.com/sharebook-kr/pykiwoom
- https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/packages.html?highlight=metapackage#anaconda-metapackage
- https://www.anaconda.com/blog/whats-in-a-name-clarifying-the-anaconda-metapackage

### How do I setup pykiwoom environment?
```
(base) $ set CONDA_FORCE_32BIT=1
(base) $ conda create -n kiwoom python=3.7.9 anaconda
(base) $ conda activate kiwoom
(kiwoom) $ pip install -U pykiwoom
```
- Why `set CONDA_FORCE_32BIT=1`? https://corytips.tistory.com/206
- Why `conda create -n kiwoom python=3.7.9 anaconda`? https://lazyblue.tistory.com/9
