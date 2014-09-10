iview
=====
A quick and simple image viewer for Linux, based on Python and Qt

Requirements
------------
Running iview requires Qt and PyQt installed. iview program is a
single python file.

Usage
-----
Calling iview requires specifying one or more image file names.
When a single file is specified the list of all files with a known
extension in the same directory is used as image list for prev/next.

Key bindings
------------
- "F1" : Help on key bindings
- Left arrow : previous file
- Right arrow : next file
- "1", "2", "3", "4" : Sets exact 1/1, 2/1, 3/1 or 4/1 pixel scaling
- "0", Home : Zoom image to fit view
- "F" : Fullscreen on/off
- "R" : Rotate image
- "E" : Ellipse markup mode ("1"-"9" thickness, "R"/"G"/"B" color)
- "A" : Arrow markup mode ("1"-"9" thickness, "R"/"G"/"B" color)
- "T" : Text markup mode (ctrl-"1".."9" font size, ctrl-"R"/"G"/"B" color)
- "Y" : Grayscale conversion (simply keeps green channel only)
- "M" : Measuring mode
- "C" : Crop image
- "S" : Save image as
- "U" : Undo unsaved changes (rotation/crop/markup)
- "F2" : Rename current file
- "Del" : Delete current file

Mouse drag does panning, mouse wheel does zooming.

Features
--------
- Smooth scaling when zooming out, hard scaling when zooming in
- When changing to next/prev picture the view is not changed if
  picture size is the same (allows looking at several images as
  an animation)
- Updating the image on disk updates the view (live display)
- Zoom is centered on mouse position
- Transparency support, measuring mode
- Rotation, cropping, simple markup and format conversion
  with "save as..."
- Supports most image formats (anything QImage accepts).
  On my system the list of known extensions is:
  bmp, bw, bw, dds, eps, eps, epsf, epsf, epsi, epsi, exr, exr,
  gif, ico, jp2, jpeg, jpg, mng, pbm, pcx, pcx, pgm, pic, png,
  ppm, psd, psd, ras, ras, rgb, rgb, rgba, rgba, sgi, sgi, svg,
  svgz, tga, tga, tif, tiff, xbm, xcf, xcf, xpm, xv.
- PGM file writing (strangely unsupported by QImage)
- Running with --screenshot [filename] takes a full desktop
  screenshot and opens it