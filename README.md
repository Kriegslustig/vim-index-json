# Vim index.json

index.json contains all default mappings for all modes.

This basically vims ':help index' as a JSON file. I originally created this for "vim-shortcut-viewer"

Substitutions used to generate it:
```
:%s/"/\\"/g
:%s/\v\n\|[^\|]+\|\s+([^\t]+)\t+(.*)/\r"\1": "\2",/
:%s/\v\n\t+/
%s/\v(\n\s{4}".*)CTRL\-([^" }]{1,2})(.*":)/\1<C-\2>\3/
:%s/{\(0-9a-z\\"%#\*:=\)}/([0-9a-z\\"%#\\\\*:=])/
:%s/\v(\n\s{4}".*)\{char\d?\}(.*":)/\1(\\w)\2/
```
I then still had to do some cleaning up by hand. Bacause Foobar.


