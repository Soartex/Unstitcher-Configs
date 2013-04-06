#Unstitcher Config Repository
### An easy way to upgrade a texture pack from 1.4.7 to 1.5.1
***
This is a central repo of all the community made configs. These are all used alongside the soartex community made unstitcher. Below is an example of a config.

    (Iron Chest Example)
    output=/mods/ironchest/textures/blocks/
    
    1.1=iron_side
    1.2=iron_top

    2.1=gold_side
    2.2=gold_top

### How to Use (Coming Soon)
***

### A Breakdown of Things for Config File Creators
***
    output=
This is the base path that the images will be output to upon unstitching. Almost all mods will now have a format that
consists of /mods/(modname)/textures/(typeoftexture)
*The value of this will always be a string starting and ending with /*

    1.1=
    ...
    16.16=
This is the heart of the config file. It contains the name of the texture minus the .png extension.
The numbers 1.1= is the location of the image. This goes from 1.1 at the top left to 16.16 at the bottom right.

A few examples and explanations.

    1.1=block
    1.2=subfolder/item
    1.3=#
    1.4=
1.1= Will give the unstitched image at 1.1 the name block and place it in the base path given to output=

1.2= Will place the unstitched image at 1.2 into a subfolder named subfolder in the base path and give it the name item

1.3= Will place the unstitched image at 1.3 into a subfolder named Unknown and give it a number ranging from 1-256 based on its location on the original sprite sheet.

1.4= Will skip the image at 1.4. This is the same as deleting the line entirely from the file.


The Unstitcher has the ability to output one location to multiple filenames also.

For example:

    1.1=block
    1.1=item
This will make two copies of the texture at 1.1 one named block and one named item. You can find an example of this with the [IC2 crops.config](http://github.com/Soartex-Fanver/Unstitcher-Configs/blob/master/ic2/sprites/crops_0.config)


When you have finished creating your config file it should be given the name of the original sprite sheet with a .config extension rather than a .png extension, and placed in a folder structure same as the original 1.4.7 sprite sheet [Like this](http://github.com/Soartex-Fanver/Unstitcher-Configs/blob/master/gfx/forestry/blocks/arboriculture.config)

Final step is uploading your config for others to use either at the [feed-the-beast forums](http://forum.feed-the-beast.com/threads/mod-texture-unstitcher-wip.17460/), the [Soartex forums](http://soartex.net/threads/mod-texture-conversion-to-1-5.521/), or fork the repo and submit a pull request. :D
