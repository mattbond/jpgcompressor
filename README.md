Titanium JPGCompressor
======================

Author: Philipp Fehre [Website](http://sideshowcoder.com)
Repository: https://github.com/sideshowcoder/jpgcompressor

Description
-----------
### Compression
Passing through UIImageJPEGRepresentation option to compress and scale images
passed as a TiBlob. The resulting image is write to e temporary file if the
name is passed as a secound argument or passed back as a TiBlob if no name is
given.

The compression quality is calculated by check the received data size against
the desired size the ratio is taken as the compression factor. If wortQuality
limit is set it is the take as the compression factor if the ratio calculated
drops below.

#### Example
100kb Image desired 50kb compressed -> compression factor 0.5
100kb Image desired 50kb compressed, worst quality set to 0.6 -> compression factor 0.6

### Scaling
Scale images using UIGraphicsBeginImageContext to fit the image in the desired size

Usage
-----
See `example/app.js` and https://github.com/sideshowcoder/jpgcompressor/blob/master/documentation/index.md

Testing
-------
Run the example app and follow it's log see `example/app.js` for more details

Setup
-----
Install the CLI tools via `npm install appcelerator -g` and install the needed 
sdk after by running `appc setup` and `titanium sdk install 3.5.0.GA`. Now you can 
build the module by going into the folder and run `python build.py`.

NOTE: Depending on your python setup it might complain about missing `markdown` 
This can be solved by running `sudo easy_install markdown`

