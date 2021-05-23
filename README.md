# doppler

This is a shell script which creates and displays an animated rainfall radar map for the previous two hours over Ireland. 

It first pulls down the last eight static rainfall radar images from the met eireann website. These images are `.png` image files and are updated every 15 minutes. It will then stitch them together, using the `convert` utility from `ImageMagick`, into an animnated gif. It then uses `mpv` to play the animated gif back once. 

As there are eight images, taken 15 minutes apart, the gif represents a two hour time span. 

## Dependencies

* ImageMagick
* mpv
* curl

It has been tested and works in the z shell on Arch Linux. It probably works in other shells but I haven't tested it. 
