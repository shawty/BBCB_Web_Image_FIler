# BBCB Web Image Filer
A HTML based mini application, written in JavaScript to allow you to host BBC B Screen images on a website and view them.

# What is it?
A very simple JavaScript based single page app that allows you to specify a list of RAW Binary BBC Model B screen dump images, and display them, save the converted image and download the raw image in it's original format.

# How to use it
There are 2 files 'index.html' and 'screens.json'.

index.html is the main viewing HTML page, drop it in a web accessable folder on your web server, then access it via a browser as you would for any normal web page.  DO BE AWARE though, that it does use Twitter Bootstrap and some modern HTML5 tech such as flexbox to help with the layout and styling, and it does require JavaScript to work too, so it needs a reasonably modern browser circa the last 5 years or so.

**PLEASE NOTE:** it CANNOT be run directly from disk, as the security model built into modern browsers will not allow the code in the page to load the screens.json file.  There are ways round this, by embedding the json data directly in the HTML web page, however you will still then have the same problem loading the disk images, if your running this locally you'll need to run it via a server such as "Apache", "Nginx", "Light HTTPD" or "IIS".

open the 'screens.json' file in a text editor of your choice, and you'll see that it's a simple javascript data format.

Each line is enclosed in [] and seperated by commas, each line forms a single javascript object that describes a single screen image EG:

    { "name": "MODE0.bin", "description": "Mode 0 test screen", "mode": 0 },

in this example, the screen image name is "MODE0.bin" the description (Displayed in the table in the HTML) is "Mode 0 test screen" and the screen mode the image was created in is mode 0.

once you've listed your screens in 'screens.json', place the file in the same folder as your html file, create a folder called 'screens' and add your images into that folder.

When done, point your browser at the server you placed it on, and you should be able to see your disks and thier contents listed.

Using it is quite simple, click view and the screen will appear at the bottom of the list (You might have to scroll if it's a long list) , click "download unconverted" and you'll get a download of the raw data, and right click on the image displayed on the page, and use "save image as" if you want a copy of the image as a modern PNG file.

# Bonus Stuff
There are some easy to read JavaScript data chunks in the page code to set up modes and palettes, it should be quite easy to add new  screen modes to the page, and the palettes can be changed to any valid RGBA (Red, Green, Blue, Alpha) values you like as the output images are 24Bpp true colour images with an alpha channel.

# Help?
As with much of the stuff like this, I really don't have any time to support it, what you see is what you get and I assume a reasonable level of technical competence by anyone playing with any of this stuff.

That said, you can generally get an answer from me as "@shawty_ds" on Twitter, or as "shawty.d.ds@googlemail.com" on GMail if your totally and hoplesly stuck.
