**ASE2GPL** is a Python script that converts Adobe Swatch Exchange (ASE)
palettes in a directory into GIMP'S GPL format. The converted palettes are outputted
to a gpl directory inside the palettes directory.

This script was [originally written in 2008 by Chris Mohler][ORIGINAL] for Kuler's palette 
exports. It was [updated by Roy Curtis][ROY]  in 2018 [after an issue report on reddit
by /u/Adderbox76][REDDIT].


This script allows ASE palettes exported from [Adobe's Color Creative Cloud (formerly
Kuler)][KULER] to be converted to GPL files.

# Usage

The script was modified to convert all .ase palettes inside a specified directory, any othre file will
be ignored, the converted palettes will be otputted into a gpl directory inside the specified directory.
To execute the script just run a python2.7 command line, execute with the python command and pass a path
to the script and a path to the palettes directory.
 
`python /path/to/script-dir/ASE2GPL.py /path/to/palettes/dir`


Note that if the ASE file has multiple palettes (as is possible, according to the spec),
each palette will be imported as its own new palette file.

# Issues

* Palettes that use CMYK and LAB colors will convert to RGB inaccurately, meaning some of
the colors may be off by one or two values. The plugin will warn you about this.
* Grayscale palettes are not yet supported
* The code is not exactly clean or DRY...

# Notes

References used for the ASE format:

* http://carl.camera/default.aspx?id=109
* http://www.selapa.net/swatches/colors/fileformats.php#adobe_ase
* https://bazaar.launchpad.net/~olivier-berten/swatchbooker/trunk/view/head:/src/swatchbook/codecs/adobe_ase.py

... and their archives, if they become lost to history:

* http://archive.is/C2Fe6
* http://archive.is/jFiTU
* http://archive.is/AEB9m


[ORIGINAL]: http://registry.gimp.org/node/10325
[ROY]: https://github.com/RoyCurtis/ASE2GIMP
[REDDIT]: https://www.reddit.com/r/GIMP/comments/80t574/kuler_palettes_to_gpl/
[KULER]: https://color.adobe.com/
[1]: https://i.imgur.com/lvaIRTi.jpg
[2]: https://i.imgur.com/BLrLMSo.jpg
[3]: https://i.imgur.com/fbsU3Rx.jpg
[4]: https://i.imgur.com/DgJ62g0.jpg