## Category

### What should I read first?
- http://vimdoc.sourceforge.net/htmldoc/usr_toc.html

### How do I configure ~/.vimrc?
```
set autoindent
filetype plugin indent on

set number

set expandtab
set shiftwidth=4
set softtabstop=4
set tabstop=4
 
syntax on
```

### How do I fix indentation?
- `gg=G`: https://stackoverflow.com/questions/506075/how-do-i-fix-the-indentation-of-an-entire-file-in-vi
  - `gg`: Go to the start of a file - http://vimdoc.sourceforge.net/htmldoc/usr_03.html
  - `=`: Re-indent the lines - http://vimdoc.sourceforge.net/htmldoc/usr_30.html
  - `G`: Go to the end of the file - http://vimdoc.sourceforge.net/htmldoc/usr_03.html

### Should I learn vi now?
https://www.tecmint.com/reasons-to-learn-vi-vim-editor-in-linux/

### How do I split window?
- `:split`, `:vsplit` - http://vimdoc.sourceforge.net/htmldoc/usr_08.html

### What is this window?
![image](https://user-images.githubusercontent.com/28881330/76966857-f02a2d80-6969-11ea-8f9d-c6ace9893929.png)

This is command-line window that opens when I enter `q:` by mistake.
- https://vim.fandom.com/wiki/Using_command-line_history
