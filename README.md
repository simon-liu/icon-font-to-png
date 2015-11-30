# Icon Font to PNG
[![Version](https://img.shields.io/pypi/v/icon_font_to_png.svg)](https://pypi.python.org/pypi/icon_font_to_png)
[![License](https://img.shields.io/github/license/Pythonity/icon-font-to-png.svg)](https://github.com/Pythonity/icon-font-to-png/blob/master/LICENSE)
[![Build](https://img.shields.io/travis/Pythonity/icon-font-to-png.svg)](https://travis-ci.org/Pythonity/icon-font-to-png)

Python (2 & 3 compatible) script for exporting icons from icon font
(e.g. Font Awesome, Octicons) as PNG images. It also comes with
`font-awesome-to-png` script for backward compatibility.

Packages required for running  and testing are listed in `requirements` directory.

## Installation
Make sure you have required packages for [Pillow installation](https://pillow.readthedocs.org/en/3.0.x/installation.html).

With `pip` (recommended):
```
$ pip install icon_font_to_png
```

Without `pip`:
```
$ git clone https://github.com/Pythonity/icon-font-to-png
$ pip install -r icon-font-to-png/requirements.txt
$ cd icon-font-to-png/bin
```

## Usage
```
usage: icon-font-to-png [-h] [--list] [--download {font-awesome,octicons}]
                        [--ttf TTF-FILE] [--css CSS-FILE] [--size SIZE]
                        [--scale SCALE] [--color COLOR] [--filename FILENAME]
                        [--keep_prefix]
                        [icons [icons ...]]

Exports font icons as PNG images.

optional arguments:
  -h, --help            show this help message and exit
  --list                list all available icon names and exit
  --download {font-awesome,octicons}
                        download latest icon font and exit

required arguments:
  --ttf TTF-FILE        path to TTF file
  --css CSS-FILE        path to CSS file

exporting icons:
  icons                 names of the icons to export (or 'ALL' for all icons)
  --size SIZE           icon size in pixels (default: 16)
  --scale SCALE         scaling factor between 0 and 1, or 'auto' for
                        automatic scaling (default: auto); be careful, as
                        setting it may lead to icons being cropped
  --color COLOR         HTML color code or name (default: black)
  --filename FILENAME   name of the output file (without '.png' extension);
                        it's used as a prefix if multiple icons are exported
  --keep_prefix         do not remove common icon prefix (i.e. 'fa-arrow-
                        right' instead of 'arrow-right')

```

## Examples
Download latest Font Awesome:  
`$ icon-font-to-png --download font-awesome`

List all available icons:  
`$ icon-font-to-png --css font-awesome.css --ttf fontawesome-webfont.ttf --list`

Export 'play' and 'stop' icons, size 64x64:  
`$ icon-font-to-png --css font-awesome.css --ttf fontawesome-webfont.ttf --size 64 play stop`

Export all icons in blue:  
`$ icon-font-to-png --css font-awesome.css --ttf fontawesome-webfont.ttf --color blue ALL`

Or you can use `font-awesome-to-png`, which works analogously:  
`$ font-awesome-to-png ALL`

## Tests
Package was tested with `tox` on Python 2.7 and Python 3.4 (see `tox.ini`).

To run tests yourself, just run `tox` inside repository.

## Contributions
Package source code is available at [GitHub](https://github.com/Pythonity/icon-font-to-png).

Feel free to use, ask, fork, star, report bugs, fix them, suggest enhancements
and point out any mistakes.

## Authors
Developed and maintained by [Pythonity](http://pythonity.com/).

Original version by [Michał Wojciechowski](https://github.com/odyniec), 
refactored by [Paweł Adamczak](https://github.com/pawelad).
