linux
======

How to enable Ctrl-L to clear screen when 'set -o vi' is set?
--------------------------------------------------------------
According to https://unix.stackexchange.com/questions/104094/is-there-any-way-to-enable-ctrll-to-clear-screen-when-set-o-vi-is-set
::

    set -o vi
    bind -m vi-command 'Control-l: clear-screen'
    bind -m vi-insert 'Control-l: clear-screen'
