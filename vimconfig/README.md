# vimconfig

File `~/.vimrc`

## Disable default visual block mode

```
# Disable default visual block mode
source $VIMRUNTIME/defaults.vim
set mouse-=a
```

## Converting tabs to spaces

```
# Converting tab to 4 spaces
set expandtab tabstop=4 shiftwidth=4
```

```
# Converting tab to <NUM_OF_SPACES> spaces
set expandtab
set tabstop=<NUM_OF_SPACES>
set shiftwidth=<NUM_OF_SPACES>
```

