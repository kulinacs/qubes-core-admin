=======
qvm-run
=======

NAME
====
qvm-run - run a command on a specified VM

SYNOPSIS
========
| qvm-run [options] [<vm-name>] [<cmd>]

OPTIONS
=======
-h, --help
    Show this help message and exit
-q, --quiet
    Be quiet           
-a, --auto
    Auto start the VM if not running
-u USER, --user=USER
    Run command in a VM as a specified user
--tray
    Use tray notifications instead of stdout
--all
    Run command on all currently running VMs (or all paused, in case of --unpause)
--exclude=EXCLUDE_LIST
    When --all is used: exclude this VM name (might be repeated)
--wait
    Wait for the VM(s) to shutdown
--shutdown
    (deprecated) Do 'xl shutdown' for the VM(s) (can be combined this with --all and --wait)
--pause
    Do 'xl pause' for the VM(s) (can be combined this with --all and --wait)
--unpause
    Do 'xl unpause' for the VM(s) (can be combined this with --all and --wait)
-p, --pass-io
    Pass stdin/stdout/stderr from remote program
--localcmd=LOCALCMD
    With --pass-io, pass stdin/stdout/stderr to the given program
--nogui
    Run command without gui
--filter-escape-chars
    Filter terminal escape sequences (default if output is terminal)
--no-filter-escape-chars
    Do not filter terminal escape sequences - overrides --filter-escape-chars, DANGEROUS when output is terminal
--no-color-output
    Disable marking VM output with red color
--no-color-stderr
    Disable marking VM stderr with red color
--color-output
    Force marking VM output with given ANSI style (use 31 for red)
--color-stderr
    Force marking VM stderr with given ANSI style (use 31 for red)
--force
    Force operation, even if may damage other VMs (eg. shutdown of NetVM)

AUTHORS
=======
| Joanna Rutkowska <joanna at invisiblethingslab dot com>
| Rafal Wojtczuk <rafal at invisiblethingslab dot com>
| Marek Marczykowski <marmarek at invisiblethingslab dot com>
