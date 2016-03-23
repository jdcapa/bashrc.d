bashrc.d
========
This is the directory to my `.bashrc` file

Install
-------

Simply download the folder to your $HOME and add the following lines to your `$HOME/.bashrc` file:

```bash
if [ -d $HOME/.bashrc.d ]; then
    for x in $HOME/.bashrc.d/* ; do
        test -f "$x" || continue
        test -x "$x" || continue
        . "$x"
    done
fi
```

The bashrc.d/ files with an `x` flag (`chmod +x <file>`) will be executed during the bash initialisation.
This is a modified version of something described by [chisel] (http://blogs.perl.org/users/chisel/2011/08/managing-my-shell-setup.html).
