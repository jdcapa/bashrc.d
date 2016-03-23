bashrc.d
========

This is the directory to my `.bashrc` file.
In the directory, all necessary bash options, paths, aliases and functions are
 provided through the respective files.
Through this, it is now simpler to add modifications and turn on/off certain
 bash functionalities.
Additionally, it is much quicker to distribute this bash set-up to various
 remote machines.


Install
-------

Simply clone the .bashrc.d directory to your `$HOME` via:

    $ git clone https://github.com/jdcapa/bashrc.d.git $HOME/.bashrc.d

Now update your `$HOME/.bashrc` file via:

    $ cat $HOME/.bashrc.d/bashrc.init >> $HOME/.bashrc


The `bashrc.d/*` files with an **`x`** flag (`chmod u+x <file>`) will be
 executed during the bash initialisation.
Therefore, if you want additional functionality, just add an executable bash
 file to your `bashrc.d/`.
It should be noted that in the current set-up, the `$PATH` and related
 variables get exported in stage 7.
Hence, everything concerning the path or library_path environment variables
 should be set in stage 6.


Sources
-------

This is a modified version of the *.bashrc.d method* described by
 [chisel](http://blogs.perl.org/users/chisel/2011/08/managing-my-shell-setup.html).

