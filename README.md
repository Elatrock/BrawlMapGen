[![Latest tag](https://img.shields.io/github/v/tag/thedonciuxx/brawlmapgen?label=version)](https://github.com/thedonciuxx/BrawlMapGen/tags)
[![Build](https://img.shields.io/github/workflow/status/thedonciuxx/BrawlMapGen/Multi-platform%20build)](https://github.com/thedonciuxx/BrawlMapGen/actions/workflows/build.yml)
[![GitHub issues](https://img.shields.io/github/issues/thedonciuxx/brawlmapgen)](https://github.com/thedonciuxx/BrawlMapGen/issues)
[![GitHub stars](https://img.shields.io/github/stars/thedonciuxx/BrawlMapGen)](https://github.com/thedonciuxx/BrawlMapGen/stargazers)
![Vector count](https://shields-staging.herokuapp.com/github/directory-file-count/thedonciuxx/brawlmapgen/assets/tiles/brawlstars?type=file&extension=svg&label=tiles%20(excluding%20water))
[![GitHub license](https://img.shields.io/github/license/thedonciuxx/BrawlMapGen)](https://github.com/thedonciuxx/BrawlMapGen/blob/master/COPYING)

# BrawlMapGen
BMG (also known as AMG - Advanced Map Generator) is a generator which takes arrays of strings and tiles with vector graphics to make generated map images of any size.

## Compiling
You can use the built versions in found in tags. Each tag has a build for any of the major operating systems.
<br>To build the program yourself, open `BMG.sln`, switch to the "Release" configuration and press Build → Build Solution.

## Requirements
###### Linux:
[SVG](https://github.com/vvvv/SVG) uses the Microsoft Graphics Device Interface (GDI), which is required to run the program.
<br>```cd «BMG-FOLDER»```
<br>```apt-get update && apt-get install -y apt-utils libgdiplus libc6-dev```

Then, if not already, give `BMG` permission to be executed.
<br>```chmod +x BMG```

Note: BMG runs in reference to the working directory, make sure the `cd` is set to the folder where `./BMG` is located before running so that issues are minimized.

## Running
Before opening the built application, notice the `options.json` which should be provided in the repository's root folder, to use the file make sure it's in the same folder as the executable. The provided file contains some generation data. Play around with the settings to understand it better!

For information about what game modes, biomes, tiles, etc. can be set in the `options.json` file, you can find [here](https://github.com/thedonciuxx/BrawlMapGen/wiki/OPTIONS-Format-1).

Most documentation is on the [wiki](https://github.com/thedonciuxx/BrawlMapGen/wiki).

###### Windows:
Run the `BMG.exe` program found in the folder.

###### Linux / macOS:
Open up a terminal on the BMG folder and run `./BMG`

#### Generation steps:
BMG/AMG first pre-loads every single tile found in the chosen preset file, doing a pass through every file for each different tileSize you set in `options.json`.

**The bigger the tilesize, the longer it's going to do a pass, at really big values it might even fail!**

After loading in all assets, the generator starts to generate the images as fast as possible, your disk speed will have an impact on the speed of generation as after each map image is constructed, it's saved to a file and discarded from memory for efficiency and so that the RAM usage doesn't pile on.

## Contributing
BrawlMapGen, even though was named and created as a game map image generator for the video game Brawl Stars, was actually created to be expanded upon.

You are free to create, use BrawlMapGen with and share your own provided presets and assets.

Any pull requests made to improve the project are more than welcome.

## Dependencies
* [SVG](https://github.com/vvvv/SVG)
* [Newtonsoft.Json](https://github.com/JamesNK/Newtonsoft.Json)
* [System.Drawing.Common](https://www.nuget.org/packages/System.Drawing.Common)

## Licensing
BrawlMapGen is licensed under the [GNU General Public License v3.0](https://github.com/thedonciuxx/BrawlMapGen/blob/master/COPYING).

You are free to use the SVGs and map images generated by the program for both personal and commercial uses.

Crediting is not required.
