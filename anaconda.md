## Category

### What is `anaconda` in `conda create -n envname anaconda`?
- Metapackage, it collects together all the packages in the Anaconda installer.
- Useful to use https://github.com/sharebook-kr/pykiwoom
- https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/packages.html?highlight=metapackage#anaconda-metapackage
- https://www.anaconda.com/blog/whats-in-a-name-clarifying-the-anaconda-metapackage
```
(base) $ conda create -n kiwoom anaconda
(base) $ conda activate kiwoom
(kiwoom) $ pip install -U pykiwoom
```

### 
