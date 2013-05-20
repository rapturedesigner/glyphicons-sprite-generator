#Sprite Generator for Bootstrap
_Most of the credit should go to [Gavin M. Roy](https://github.com/gmr) ([@Crad](https://twitter.com/crad)) for doing such an amazing job with this script in the first place. All I did was make a few alterations and adaptions. Cheers Gavin!_

The GLYPHICONS & Icons Sprite Generator allows you to change the size and colors of the
Bootstap icons using the Free, All or Pro versions of GLYPHICONS. When using the Pro or All
files, all the extra icons will be available to your Bootstrap project.

New CSS and PNG sprites are generated that can override Bootstrap's
default icon before or mixed into a Bootstrap LESS project.

#Dependencies
The only required non-standard-library package that is needed is the Python
Imaging Library. To install this simply run:
`easy_install pil` 
or
`pip install pil` 
from the terminal.

**For Mac OSX users**, you will need to have command line tools installed from Xcode. You can find an excellent guide [here](http://blog.artooro.com/2013/01/04/how-to-install-pil-python-imaging-library-on-mac-os-x-10-8/)

#Custom Icons
You can also generate CSS and a PNG sprite from your own PNG icons.
In order to use a custom PNG iconset, your individual namespacing has to be as follows:

`[prefix]_[numbering]_[icon-name].png`

eg. `icon_0123_firetruck.png.`

**Your icons must be an a folder named 'png' for this to work**

New CSS and PNG sprites are generated that can override Bootstrap's
default icon before or mixed into a Bootstrap LESS project.

#How to use sprite-generator.py

 1. Download the type of GLYPICONS distribution and extract the zip file
 2. Copy sprite-generator.py into the extracted `glypicons_free`, `glyphicons_all` or `glyphicons_pro` folder
 3. Run sprite-generator.py; You will be asked for:
    - The `prefix` you want to use (leave blank for `glyphicons`)
    - The `RGB color` value for your `icon-white` sprite (leave blank for plain-old `white`)
    - The `preview background HEX colour`, without the `#` if you chose a custom value above (Leave blank for the default `444`)
    - The icon size `x,y` you would like in pixels (Leave blank for default `14,14`)
 4. If everything worked property, sprite-generator.py will have generated the following files in the "sprites" directory:

    - glyphicons.css         CSS Overrides
    - glyphicons.html        Preview HTML
    - glyphicons.png         Black Icons
    - glyphicons-white.png   White (or colorized) icons

 5. Open sprites/glyphicons.html in your browser (if you're on a Mac, it will try and do so itself)

#FAQ
###How do I use this in my Bootstrap Project?
1. Copy the newly generated glyphicons.png and glyphicons-white.png to the project img directory.
2. Include the glyphicons.css file *after* the bootstrap CSS files or include in
   your bootstrap.less files after the sprites.less entry.
3. Edit glyphicons.css, fixing the paths to the image files in the background-image directives.

###Can I Change the colour/size of the icons?
Absolutely!
When you run the `sprite-generator.py` script, you will be asked to specify these values. Leave everything blank (just hit enter) for the defaults. You'll be asked for the `icon-prefix`,`secondary,custom colour`,`preview background colour`, and `icon-size`

###Can I use my own icons?
Sure! Just copy your custom PNG icons in a folder called `png` and run the script. Please make sure your icon-namespacing is correct, I will probably update this to exclude the namespacing for custom icons soon. The correct namespace is:

`[prefix]_[numbering]_[icon-name].png`

###How do I use the nice, styled All/Pro Glyphicons from the PSD?
If you're in Photoshop (I did this with CS6, OSX 10.8), click on `File > Scripts > Export Layers to Files...`. From here you will be able to choose a destination and a prefix. 
**Remember to name your destination folder 'png' or the script won't work!**

If you **DON'T** specify a `prefix`, that's ok, You just have to remember to specify `_0` as the `prefix` in `sprite-generator.py`. This may take a while, so you might want to leave it overnight. I know there are some pretty awesome scripts out there that can do it a bit faster, but I just stuck with plain-old Photoshop.

After you have your 'png' folder, just put the `sprite-generator.py` script in the *same directory* as the png folder and run it!


#Using Glyphicons
Since you're here and if you plan on using this, you should support the designer
who made [GLYPHICONS](http://www.glyphicons.com) and pay the modest license fee for the All or Pro version. Not only
do you get more icons out of it, but whatever you're using this for will get
higher quality icons out of it. If you use the Pro icons as a source, the higher
resolution icons will be used.
