# Compiling Lua for the Nintendo 3DS

> [!IMPORTANT]
> ... should've known that Lua is already present in devkitPro's portlibs 🫠. But with this method you have control over the version you want to use in your project.

## Requirements

- [devkitPro toolchain][]
- [Lua source code][]

## Steps

1. Download `lua.patch` present in this repository.
2. Apply the patch within the installed Lua directory: `patch -p1 < lua.patch`.
4. Built with `make`.
5. Install with `sudo make install`. You might need to use `sudo` as it installs to `$DEVKITPRO/portlibs/3ds`. You can change this behavior by modifying the `Makefile`.

Assuming you are using the devkitPro `Makefile` template located at `$DEVKITPRO/examples/3ds/templates/application/Makefile` modify it to link the Lua library.

[devkitPro toolchain]: https://devkitpro.org/
[Lua source code]: https://lua.org/download.html

