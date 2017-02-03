Installation Procedure under Linux
###################################

Sketchup doesn't propose a native Linux distribution. Nonetheless, many
people use
`wine <https://appdb.winehq.org/objectManager.php?sClass=application&iId=1815>`__.
There are many tutorials already online explaining how to install
sketchup in an Ubuntu-based environment, so we're not going to go
through that again. Nonetheless, if you are having problems installing,
here is a nifty little `github project called
SkipI <https://github.com/wilfm/SkipI>`__  that can make your life a
little easier : First remove any earlier attempts at installing
Sketchup. Then open a new terminal and hit :

    ::

        wget https://raw.githubusercontent.com/wilfm/SkipI/master/skipi.sh
        chmod +x skipi.sh
        ./skipi.sh

This will install Sketchup8, which isn't the newest version, but it is
at least stable on Linux. SkipI will also configure a desktop shortcut
for you. Once in Sketchup, you may realize that .rbs folders don't work
in older Sketchup versions : you'll need a .rbz file. Making a .rbz is
fairly straightforward, as it is actually just a .zip file. So send your
T4su extension to a compressed file, then simply change the end of it's
name from .zip to .rbz. You're now ready to go to **Window >
Preferences > Install Extensions...** and select your
t4su\_version.rbz file.
