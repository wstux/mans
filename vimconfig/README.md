# vimconfig

File `~/.vimrc`

## Disable default visual block mode

```
source $VIMRUNTIME/defaults.vim
```

```
" Disable default visual block mode
set mouse-=a
```

## Converting tabs to spaces

```
" Converting tab to 4 spaces
set expandtab tabstop=4 shiftwidth=4
```

```
" Converting tab to <NUM_OF_SPACES> spaces
" On pressing tab, insert spaces
set expandtab
" Show existing tab with <NUM_OF_SPACES> spaces width
set tabstop=<NUM_OF_SPACES>
" When indenting with '>', use <NUM_OF_SPACES> spaces width
set shiftwidth=<NUM_OF_SPACES>
```

