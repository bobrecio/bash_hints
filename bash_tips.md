BASH Tips
===
#### Navigate command line with EMACS shortcuts
    - CTRL-a Beginning of Line
    - CTRL-e End of line
    - CTRL-k Cut out everything to the right of the cursor (saves in the clipboard too)
    - CTRL-m Like hitting <enter>
    - CTRL-y Paste
    - CTRL-<space> Set the mark
    - CTRL-w Copy between cursor and the "mark" into the clipboard
    - CTLR-f Forward one character
    - CTRL-b Backward one character
    - CTRL-p Previous line (in history)
    - CTRL-n Next line (in history)
    - CTRL-h Backspace
    - CTRL-_ Undo
    - CTRL-l Clear screen
#### Set key bindings to vi mode
    echo "set -o vi" >> .bashrc
#### Add a #comment string at the end of the command you type, if you want an easy bookmark to search in the command history.
    [user@host ~]$ /path/to/some_useful_script.sh #maintenance_start
    [user@host ~]$ *>CTRL-r<*
    (reverse-i-search)`maintenance_start': /path/to/some_useful_script.sh #maintenance_start
[BASH Hackers Wiki](https://wiki-dev.bash-hackers.org)

#### `date` display formats
    'date'    - Thu Aug 8 08:39:08 DST 2019
    'date +%T'    - HH:mm:ss (24 hr)
    'date +%s'    - "epoch"; seconds since 1970-01-01 00:00:00; good for general interval timing
    'date +%N'    - nanoseconds; good for small interval timing
    'date +%Y%M%d%H%M%S' - DTG (date-time group)
    