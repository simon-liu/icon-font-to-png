Icon Font to PNG
================

This program allows you to extract icons from an icon font (e.g. Font Awesome or
Octicons) as PNG images of specified size.

### Usage

    icon_font_to_png.py [-h] [--color COLOR] [--filename FILENAME]
                        [--keep-prefix] [--list] [--size SIZE]
                        ttf-file css-file icon [icon ...]

    positional arguments:
      ttf-file             the name of the TTF file
      css-file             the name of the CSS file
      icon                 the name(s) of the icon(s) to export (or "ALL" for all
                           icons)

    optional arguments:
      --color COLOR        color (HTML color code or name, default: black)
      --filename FILENAME  the name of the output file, ending with ".png" (if
                           multiple icons are exported, the value of this option
                           is used as a prefix)
      --keep-prefix        do not remove common icon prefix
      --list               list available icon names and exit
      --scale SCALE        scale (a scaling factor between 0 and 1, or "auto" for
                           automatic scaling, default: 1)
      --size SIZE          icon size in pixels (default: 16)
