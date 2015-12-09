# Vim index.json

index.json contains all default mappings for all modes.

This basically vims ':help index' as a JSON file. I originally created this for "vim-shortcut-viewer"

Substitutions used to generate it:
```
:%s/"/\\"/g
:%s/\v\n\|[^\|]+\|\s+([^\t]+)\t+(.*)/\r"\1": "\2",/
:%s/\v\n\t+/
```
I then still had to do some cleaning up by hand. Bacause Foobar.


