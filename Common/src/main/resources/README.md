# Configured Defaults

This folder is a template for your `.minecraft` directory. Place files and folders here in the same layout as
`.minecraft`, and they will be copied there when the game starts.

## How copying works

- This folder mirrors `.minecraft` one-to-one. (`.minecraft/configureddefaults/config/jei/jei.toml` is copied to
  `.minecraft/config/jei/jei.toml`)
- A file is copied only if the destination does not exist yet. Existing files are never overwritten.
- Copying runs exactly once at startup, before mods read their config files. It cannot be invoked during gameplay.

## Special case: `options.txt`

`options.txt` is handled differently. Instead of replacing it, the options listed in `configureddefaults/options.txt`
are merged into your existing `.minecraft/options.txt`. Only options that are not already present are added, so your own
settings are kept and never overwritten.

Because of this you only need to list the options you want to pre-set.

Note that the `version` field must always be present for the file to be recognized.

## Excluded files

This file (`README.md`) is never copied.
