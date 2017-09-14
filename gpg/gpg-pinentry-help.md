# GPG pinentry help

Keywords: su, ssh, pinentry, tty, curses

Treats: "No manual entry for pinentry"

## Ideas

Set the GPG agent to use TTY by editing `~/.gnupg/gpg-agent.conf` and using a line such as one of these:
 
    pinentry-program /usr/bin/pinentry-tty

    pinentry-program /usr/local/bin/pinentry-curses

Start `gpg-agent` such as:

    gpg-agent --daemon --pinentry-program /usr/local/bin/pinentry

    gpg-agent --daemon --keep-tty --use-standard-socket --pinentry-program=/usr/bin/pinentry-curses

Set environment variables such as: 

    PINENTRY_USER_DATA="USE_CURSES=1"
    export PINENTRY_USER_DATA

    GPG_TTY=$(tty)
    export GPG_TTY

Symlink

    which pinentry-curses
    /usr/bin/pinentry


