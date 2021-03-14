Swy7ch' fork of st
==================

This is my fork of suckless' terminal emulator, [st](https://st.suckless.org/). It is tweaked to match my needs and comes with just a few patches:

- [st-anysize](https://st.suckless.org/patches/anysize/)
- [st-clipboard](https://st.suckless.org/patches/clipboard/)
- [st-externalpipe](https://st.suckless.org/patches/externalpipe/)
- [st-font2](https://st.suckless.org/patches/font2/)
- [st-scrollback](https://st.suckless.org/patches/scrollback/)
- [st-xresources](https://st.suckless.org/patches/xresources/)

Keybindings
-----------

- **Alt+u / Alt+d** .....Scroll a whole page up/down
- **Alt+k / Alt+j** .....Scroll a line up/down
- **Alt+PgUp / Alt+PgDn** .....Zoom in/out
- **Alt+c** .....Copy to xclipboard
- **Alt+v** .....Paste from xclipboard
- **Alt+o** .....Copy a command output to xclipboard, through dmenu [1]
- **Alt+l** .....Follow links through dmenu [2]
- **Alt+y** .....Copy links through dmenu [2]

[1] Requires `st-copyout` from my scripts repo

[2] Requires `st-urlhandler` from my scripts repo

Colorscheme and font
--------------------

Colors, fonts and other variables are set through `xrdb`, by sourcing a
.Xresources file.

That's it!
----------

No need for anything else. Enjoy!

---

st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.


Requirements
------------
In order to build st you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

