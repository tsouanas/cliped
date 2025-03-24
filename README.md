# cliped

Write to clipboard using your favorite editor.

## Dependencies

Only dependency is `xsel` (OpenBSD already has a package for it) for
systems that run X or `pbcopy` for MacOS (which is already installed).

## Usage

If `$VISUAL` or `$EDITOR` is unset, default to `vi(1)`.

* `cliped` : create a new clip
* `cliped last` : bring up the last entry from cliped
* `cliped clean` : clean all cliped-created files

Just add some shortcut to run it via your window manager and you're set.

For example, in spectrwm I set:
```
program[cliped]      = xterm -name 'clipedterm' -title 'clipedterm' -fs 18 -e 'cliped'
program[clipedlast]  = xterm -name 'clipedterm' -title 'clipedterm' -fs 18 -e 'cliped last'
```
define the following shortcuts:
```
bind[cliped]      = MOD+i
bind[clipedlast]  = MOD+Shift+i
```
and the following quirk:
```
quirk[XTerm:clipedterm] = FLOAT
```

## Credits

Influenced by [vimclip].

[vimclip]: https://github.com/hrantzsch/vimclip

