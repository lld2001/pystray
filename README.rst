pystray Package Documentation
=============================

This library allows you to create a *system tray icon*.

Supported platforms are *Linux* under *Xorg*, *GNOME* and *Ubuntu*, *macOS*
and *Windows*.

See `here <https://pystray.readthedocs.io/en/latest/>`_ for the full
documentation.

https://github.com/moses-palmer/pystray/pull/21#issue-301853591
Icon images are stored in PNG format, which XP can not read.

See python-pillow/Pillow#1102 as the root cause.

This is a workaround allowing one to write platform independent code like:

    icon.icon =  Image.open('icon.png')
    icon.ico_path = 'icon.ico'
