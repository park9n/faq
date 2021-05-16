## Category

### What is difference between `ipython` and `jupyter`?
- `ipython notebook` project renamed to `jupyter`. Same.

### Why doesn't autocompletion work when I enter `Tab`?
```
[IPKernelApp] ERROR | Exception in message handler:
Traceback (most recent call last):
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\ipykernel\kernelbase.py", line 261, in dispatch_shell
    yield gen.maybe_future(handler(stream, idents, msg))
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\tornado\gen.py", line 762, in run
    value = future.result()
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\tornado\gen.py", line 234, in wrapper
    yielded = ctx_run(next, result)
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\tornado\gen.py", line 162, in _fake_ctx_run
    return f(*args, **kw)
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\ipykernel\kernelbase.py", line 576, in complete_request
    matches = yield gen.maybe_future(self.do_complete(code, cursor_pos))
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\ipykernel\ipkernel.py", line 356, in do_complete
    return self._experimental_do_complete(code, cursor_pos)
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\ipykernel\ipkernel.py", line 381, in _experimental_do_complete
    completions = list(_rectify_completions(code, raw_completions))
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\IPython\core\completer.py", line 484, in rectify_completions
    completions = list(completions)
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\IPython\core\completer.py", line 1818, in completions
    for c in self._completions(text, offset, _timeout=self.jedi_compute_type_timeout/1000):
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\IPython\core\completer.py", line 1862, in _completions
    full_text=full_text, cursor_line=cursor_line, cursor_pos=cursor_column)
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\IPython\core\completer.py", line 2030, in _complete
    cursor_pos, cursor_line, full_text)
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\IPython\core\completer.py", line 1374, in _jedi_matches
    text[:offset], namespaces, column=cursor_column, line=cursor_line + 1)
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\jedi\api\__init__.py", line 726, in __init__
    project=Project(Path.cwd()), **kwds)
TypeError: __init__() got an unexpected keyword argument 'column'
```
- Add `"%config Completer.use_jedi = False"`
- https://stackoverflow.com/questions/40536560/ipython-and-jupyter-autocomplete-not-working
- https://rural-mouse.tistory.com/19?category=781441

### What is difference between `Trusted` and `Not Trusted`?
- https://jupyter-notebook.readthedocs.io/en/stable/security.html#security-in-notebook-documents
- However, `"jupyter trust --reset"` doesn't work.
```
Removing trusted signature cache: C:\Users\cspark\AppData\Roaming\jupyter\nbsignatures.db
Traceback (most recent call last):
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\runpy.py", line 193, in _run_module_as_main
    "__main__", mod_spec)
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\runpy.py", line 85, in _run_code
    exec(code, run_globals)
  File "C:\Users\cspark\anaconda3\envs\hands-on-nlp\Scripts\jupyter-trust.EXE\__main__.py", line 7, in <module>
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\jupyter_core\application.py", line 254, in launch_instance
    return super(JupyterApp, cls).launch_instance(argv=argv, **kwargs)
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\traitlets\config\application.py", line 664, in launch_instance
    app.start()
  File "c:\users\cspark\anaconda3\envs\hands-on-nlp\lib\site-packages\nbformat\sign.py", line 596, in start
    os.remove(self.notary.db_file)
PermissionError: [WinError 32] 다른 프로세스가 파일을 사용 중이기 때문에 프로세스가 액세스 할 수 없습니다: 'C:\\Users\\cspark\\AppData\\Roaming\\jupyter\\nbsignatures.db'
```

### Why does `.ipynb` file look blurry?
- No idea yet.
