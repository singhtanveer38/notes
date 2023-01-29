### Add the following lines in .vimrc file and create a folder "plugged" inside "~/.vim/"

```vim
call plug#begin("~/.vim/plugged")

" Enter plugins names here

call plug#end()
```

To install plugins, run :PlugInstall inside vim

### Add the following lines in ".vimrc" before ```plug#begin()```call
```vim
" Install vim-plug if not found
if empty(glob('~/.vim/autoload/plug.vim'))
  silent !curl -fLo ~/.vim/autoload/plug.vim --create-dirs
    \ https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
endif

" Run PlugInstall if there are missing plugins
autocmd VimEnter * if len(filter(values(g:plugs), '!isdirectory(v:val.dir)'))
  \| PlugInstall --sync | source $MYVIMRC
\| endif
```
