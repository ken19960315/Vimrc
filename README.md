# Vimrc
for backup and share my vimrc file

[Traditional Chinese README](README_zh-TW.md)
# Files
- **.vimrc**          : settings for [vim](https://github.com/vim/vim)
- **init.vim**        : settings for [neovim](https://github.com/neovim/neovim)
- **installVimrc.sh** : install script for **.vimrc** and **init.vim**
# To use vimrc
open the vim and type **:help vimrc**, then it will show the help file about where to put vimrc

if you don't use neovim, just ignore the "init.vim" file

after you put vimrc in the right directory, you can type **:e $MYVIMRC** in vim to edit the vimrc file

I will talk about where I place my vimrc below as an example
## For Linux and Mac
I place the ".vimrc" at "$HOME/" and "init.vim" at "$HOME/.config/nvim/"

this is the default directory of vimrc
## For Windows
I place the "init.vim" at "$XDG_CONFIG_HOME\nvim\\"
  
as for ".vimrc", I don't use vim on Windows, so if you use neovim just place it to a directory and modify the **"source ~/.vimrc"** line in "init.vim" with the path you place ".vimrc"
  
for example, if you put ".vimrc" at "D:\Vim\\", then modify the source line as below
```
source D:\Vim\.vimrc
```
  
else read the vim help file to know where to put the ".vimrc"
# Using Install Script
the script is written in **bash** script, so any shell support bash script can be used

to use the script

- first ```chmod u+x installVimrc.sh``` to make the script executable
- modify the directory path **vimrcDir** and **nvimrcDir** if necessary,
  this is the installed directory of **.vimrc** and **init.vim** respectively
- modify the target file name **vimrcTargetFile** and **nvimrcTargetFile** if necessary,
  this is the installed file name of **.vimrc** and **init.vim** respectively
- if you don't use neovim, just comment the line ```cp ${nvimrcSourceFile} ...``` with '#' at the beginning of the line
- type ```./installVimrc.sh``` to install **.vimrc** and **init.vim** file
# Key Mappings
- Ctrl+x      : toggle the tree browser
- <Leader> r  : toggle relativenumber setting
## Neovim Specific Key Mappings
- Ctrl+s : toggle the terminal
- Ctrl+q : exit teminal mode in neovim
# Self Defined Functions
- FlotisableToggleRelativeNumber() : toggle relativenumber setting
# Plugins
- [vim-plug](https://github.com/junegunn/vim-plug)              : vim plugins manager
- [Nerdtree](https://github.com/scrooloose/nerdtree)            : to browse the directory in a tree view
- [neocomplcache](https://github.com/shougo/neocomplcache.vim)  : autocomplete plugin( I use this because my vim version is old, for newer version you can try [YouCompleteMe](https://github.com/valloric/youcompleteme) or [neocomplete](https://github.com/shougo/neocomplete.vim) )
- [tagbar](https://github.com/majutsushi/tagbar)                : to display tags( depend on ctags )
## Neovim Specific Plugins
- [neoterm](https://github.com/kassio/neoterm)                  : terminal plugin
## For ctags
ctags only support c/c++ language, for other language you can try
- [exuberant ctags](http://ctags.sourceforge.net/)            : a ctags support many language( seems not in maintenance now )
- [universal ctags](https://github.com/universal-ctags/ctags) : the continuous of exuberant ctags
