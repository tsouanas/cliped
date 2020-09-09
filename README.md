# cliped

Write to clipboard using your favorite `$EDITOR`.

## Dependencies

Only dependency is xsel (OpenBSD already has a package for it).

## Usage

If `$EDITOR` is unset, default to `vi(1)`.

* `cliped` : create a new clip
* `cliped last` : bring up the last entry from cliped
* `cliped clean` : clean all cliped-created files

Just add some shortcut to run it via your window manager and you're set.
For example, in spectrwm I set:
```
program[cliped]      = xterm -title 'cliped' -e 'cliped'
program[clipedlast]  = xterm -title 'cliped' -e 'cliped last'
bind[cliped]         = MOD+i
bind[clipedlast]     = MOD+Shift+i
```

## Credits

Based on / influenced by: @hrantzsch 's vimclip:
https://github.com/hrantzsch/vimclip

