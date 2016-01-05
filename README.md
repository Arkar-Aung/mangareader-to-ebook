Mangareader to ebooks support epub and pdf format.

Requirement
===========

* python 2.7
* Python Image Library if using --resize

Credit
======

* mdl.py is base on [mdl.rb](https://github.com/lukaszkorecki/mdl)

Download Images from mangareader.net
====================================

	$python mdl.py <START URL> <OUTPUT DIR> 

Example :

	$python mdl.py http://www.mangareader.net/bleach/482 Bleach

or

	$python mdl.py http://www.mangareader.net/bleach/482 ./

Make epub
=========

	$python makepub.py <dir>

Default image format is jpg. Use --ext to specify another

Example :

	$python makepub.py Bleach_482

or

    $python makepub.py Bleach_482 --ext png

You will get epub file in output folder


You can provide multiple folders :

    $python makepub.py Bleach_480 Bleach_481 Bleach_482

or even (linux only) :

    $python makepub.py Bleach/*/

Bleach/ being the folder containing chapter folders


You can resize images to fit your e-reader resolution with --resize width height

Example for a kobo touch:

    $python makepub.py Bleach_482 --resize 600 800

Use this to get best quality when your e-reader has lower resolution than original image's
Only available with jpg image format


Make PDF
========

	$python makePDF.py <dir> <image format>
	
Example :

	$python makePDF.py Bleach_482 jpg
	

Rename Downloaded Manga
=======================

You can rename programmatically to well-organized version by using [this shell script](https://gist.github.com/Arkar-Aung/cb9ae27ad53e1e3fd115).

        $/bin/bash rename.sh <path> <extension>
        
Example : 
      
        $/bin/bash rename.sh /home/me/manga/bleach .jpg
