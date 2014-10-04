vim-startup
===========

![vim startup script](http://dl.dropbox.com/u/185133/vim-startup/screenshot.jpg)

If you:

 * want to start with vim
 * have no time to learn how to configure it for you
 * have no time to find plugins for you


This is example startup vim configuration using vundle plugin manager and example .vimrc file.
This .vimrc is compilation other config files i have seen and my needs and preferences cut down to minimal but working version.


Installation
------------
To full work you need installed:

 * vim or vim-gtk
 * sudo apt-get install exuberant-ctags
 * for good python syntax checking install 'sudo easy_install flake8'

```bash
    # initial dirs

    mkdir -p ~/.vim/backup
    mkdir -p ~/.vim/bundle

    # plugin manager

    git clone git://github.com/Shougo/neobundle.vim ~/.vim/bundle/neobundle.vim

    # get .vimrc

    wget https://raw.github.com/onjin/vim-startup/master/.vimrc -O ~/.vimrc

    # vim fonts

    mkdir -p ~/.fonts
    wget https://github.com/onjin/vim-startup/raw/master/fonts/Anonymous%20Pro.ttf -O ~/.fonts/Anonymous\ Pro.ttf
    wget https://github.com/onjin/vim-startup/raw/master/fonts/Inconsolata.otf -O ~/.fonts/Inconsolata.otf

    # run vim

    gvim
````

Help
----

 * F3        - strip trailing white spaces
 * F4        - tagbar toggle
 * Shift+F4  - unite outline
 * F5        - paste mode toggle
 * F6        - check complexity
 * F12       - errors window toggle
 * Shift+F12 - fix pep8 errors

gui:

 * Shift+F6  - guifonts Anonymous Pro 12
 * Shift+F7  - guifonts Inconsolata 12
 * Shift+F8  - guifonts monospace 12

shell:

 * ctrl+s    - run vim shell as pop

unite:

 * ctrl+p    - search files
 * <space>p  - search files - nosplit
 * <space>/  - search in files
 * <space>s  - switch buffer
 * <space>y  - yank history
 * <space>l  - last edited files

git (fugitive):

 * ,gs       - git status
 * ,gc       - git commit
 * ,gd       - git diff
 * ,gb       - git blame

windows:

 * <ctr>+J   - switch && maximize window
 * <ctr>+K   - switch && maximize window

 * <ctr>+n   - hlsearch toggle
 * ,l        - set list toggle

vimrc:

 * ,re       - edit ~/.vimrc
 * ,rt       - open ~/.vimrc in tab
 * ,rc       - reload ~/.vimrc
 * ,rh       - edit ~/.vimrc at mapping help

buffers:

 * ,c        - close current buffer
 * ,wc       - write & close current buffer
 * ,d        - go previous buffer && close current
 * ,D        - close all buffers
 * ,,        - switch between last two buffers

python-mode plugins bindings:

 * K         - Show python docs (g:pymode_doc enabled)
 * <C-Space> - Rope autocomplete (g:pymode_rope enabled)
 * <C-c>g    - Rope goto definition (g:pymode_rope enabled)
 * <C-c>d    - Rope show documentation (g:pymode_rope enabled)
 * <C-c>f    - Rope find occurrences (g:pymode_rope enabled)
 * <Leader>r - Run python (g:pymode_run enabled)
 * <Leader>b - Set, unset breakpoint (g:pymode_breakpoint enabled)
 * [[        - Jump on previous class or function (normal, visual, operator modes)
 * ]]        - Jump on next class or function (normal, visual, operator modes)
 * [M        - Jump on previous class or method (normal, visual, operator modes)
 * ]M        - Jump on next class or method (normal, visual, operator modes)
 * aC C      - Select a class. Ex: vaC, daC, dC, yaC, yC, caC, cC (normal, operator modes)
 * iC        - Select inner class. Ex: viC, diC, yiC, ciC (normal, operator modes)
 * aM M      - Select a function or method. Ex: vaM, daM, dM, yaM, yM, caM, cM (normal, operator modes)
 * iM        - Select inner function or method. Ex: viM, diM, yiM, ciM (normal, operator modes)
