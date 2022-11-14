# doppler

This is a shell script which creates and displays an animated rainfall radar map for the previous two hours over Ireland. 

It first pulls down the last eight static rainfall radar images from the met eireann website, met.ie. These images are `.png` image files and are updated every 15 minutes. It will then stitch them together, using the `convert` utility from `ImageMagick`, into an animnated gif. It then uses `mpv` to play the animated gif back once. 

As there are eight images, taken 15 minutes apart, the gif represents a two hour time span. 

## Dependencies

* ImageMagick
* mpv
* curl

The script is POSIX compliant and has been tested and works in the z shell on Arch Linux. 

It will need to be chmod'd to give it executable privileges and put in a folder that is in the PATH environment.  

As part of the cleanup routine, it assumes that there are no files named doppimg*.png or radar.gif that are critical and cannot be deleted from the current directory.
