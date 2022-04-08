linux
======

How to enable Ctrl-L to clear screen when 'set -o vi' is set?
--------------------------------------------------------------
According to https://unix.stackexchange.com/questions/104094/is-there-any-way-to-enable-ctrll-to-clear-screen-when-set-o-vi-is-set
::

    set -o vi
    bind -m vi-command 'Control-l: clear-screen'
    bind -m vi-insert 'Control-l: clear-screen'

How to disable hyperthreading from within Linux (no access to BIOS)
--------------------------------------------------------------------
Refer to: https://serverfault.com/questions/235825/disable-hyperthreading-from-within-linux-no-access-to-bios
::

    cat /sys/devices/system/cpu/cpu*/topology/thread_siblings_list | \
    awk -F, '{print $2}' | \
    sort -n | \
    uniq | \
    ( while read X ; do echo $X ; echo 0 > /sys/devices/system/cpu/cpu$X/online ; done )
