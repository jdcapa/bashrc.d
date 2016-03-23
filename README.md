bashrc.d
========
This is the directory to my `.bashrc` file. 
In the directory, all necessary bash options, paths, aliases and functions are provided through the respective files.

Install
-------

Simply clone the .bashrc.d directory to your `$HOME` via:

`git clone https://github.com/jdcapa/bashrc.d.git $HOME/.bashrc.d` 

Now update your `$HOME/.bashrc` file via:

`cat $HOME/.bashrd.d/bashrc.init >> $HOME/.bashrc`

**Make sure `bashrc.init` is not executable; otherwise you will create a loop.**
Since the lines added to the `$HOME/.bashrc` contain the following.

```bash
if [ -d $HOME/.bashrc.d ]; then
    for x in $HOME/.bashrc.d/* ; do
        test -f "$x" || continue
        test -x "$x" || continue
        . "$x"
    done
fi
```

Hence, the bashrc.d/ files with an `x` flag (`chmod +x <file>`) will be executed during the bash initialisation.


Sources
-------
This is a modified version of the *.bashrc.d method* described by [chisel] (http://blogs.perl.org/users/chisel/2011/08/managing-my-shell-setup.html).
