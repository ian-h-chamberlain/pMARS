# pMARS

This repository is mostly archival and takes its source originally from [the pMARS SourceForge page](https://sourceforge.net/projects/corewar/).

Some small changes have been committed on top of that source to work better with git and modern macOS, since I couldn't find any other repos with an updated version.

The original README is kept [here](./README.orig.txt) for posterity.

## Building

Build status is "works on my machine" (macOS Catalina 10.15.6).

Requirements:

- XQuartz/X11. My installation builds with `-L/opt/X11/lib` and `-I/opt/X11/include`, yours may have a different installation path.
- GCC. I couldn't get it to build with Apple-provided `clang` but `gcc-10` from Homebrew seems to work okay.

To build, simply:

```sh
cd src/
make
```

This should leave an executable `pmars` in the `src` directory which can be tested against the warriors in `warriors`, e.g.

```sh
./pmars ../warriors/validate.red
```

## Documentation

You can probably just `man doc/pmars.6` for the quick and easy way. If you want to build the docs for some reason:

```sh
cd doc/
make
```

The built man page can be viewed with `man ./pmars.man`, or you can try to use a word processor to read `pmars.doc` - but that didn't seem to work too well for me.
