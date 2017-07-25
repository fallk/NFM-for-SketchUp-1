NFM-for-SketchUp
================

[Need for Madness](http://www.needformadness.com/developer/) is a fun, fast-paced car game written in Java. This SketchUp plugin helps creating vehicles for the game.

Latest Version: **0.7.2**

## Plugin Installation

The NFM plugins is a single-file. In a nutshell, you just put the file in SketchUps' Plugins folder.

* Step 1 -
    Download the [nfm-exporter.rb](https://raw.github.com/jimfoltz/NFM-for-SketchUp/master/nfm-exporter.rb) file. (Right-click link, select the *Save  As* option).

* Step 2 - Move or copy the `nfm-exporter.rb` file to your SketchUp/Plugins folder.

    For SketchUp on Windows, plugins are located here:

	* SketchUp 2016: `C:\Users\YOUR USERNAME\AppData\Roaming\SketchUp\SketchUp 2016\SketchUp\Plugins`
	* SketchUp 2015: `C:\Users\YOUR USERNAME\AppData\Roaming\SketchUp\SketchUp 2015\SketchUp\Plugins`
	* SketchUp 2014: `C:\Users\YOUR USERNAME\AppData\Roaming\SketchUp\SketchUp 2014\SketchUp\Plugins`
	* SketchUp 2013:
		* `C:\Program Files\SketchUp\SketchUp 2013\Plugins` (32-bit)
		* `C:\Program Files (x86)\SketchUp\SketchUp 2013\Plugins` (64-bit)
	* SketchUp 8 and older:
		* `C:\Program Files\Google\Google SketchUp #\Plugins` (32-bit)
		* `C:\Program Files (x86)\Google\Google SketchUp #\Plugins` (64-bit)

    (You will need Admin priviledges)    
    
	and on OSX:

        /Library/Application Support/Google SketchUp 8/SketchUp/Plugins/

* Step 3 -
    Restart SketchUp. The plugin will be in the **Plugins > Need for Madness** menu.

## Creating a Model

Download this [Sample SketchUp Model](http://sketchup.google.com/3dwarehouse/details?mid=196de521c5d5c3f0b73ce25f042b849a) to get started.

### Things to note:

* The car code is generated strictly from Faces - other SketchUp entities such as Groups and Components may be in the model, but are ignored.
* The car is centered (more or less) on the origin.
* The size of the car is appropriate for the default wheels.
* The stats and physics of the car are not included.
* Pay special attention to the names of the Materials in SketchUp - they control things like default colors, headlights, brakelights, glow, and flash. The following special names are supported as SketchUp Material names:
 * 1stColor
 * 2ndColor
 * glass
 * flash
 * glow
 * lightF
 * lightB
 * noOutline
 * far
 * near

Multiple special names can be used for any material, separated by spaces.

## Exporting Car Codes

* Select *Show Code* from SketchUp's **Plugins > Need for Madness > Show Code** menu item.
  * Click *Refresh* if you need to.
* Copy and paste the code into the NFM Car Maker code editor.
* Press Save & Preview.

If a surface is selected, only the selected surface is displayed in the dialog. Otherwise, the plugin tries to generate the polys for every surface in the model.

# Extras

## Importing Car Codes

* Select *Show Code* from SketchUp's **Plugins > Need for Madness > Show Code** menu item.
* Paste your existing code into the text box and click 'Import'

### Caveats

* Scale will be lost.
* Attributes/collision will be lost.

## Changelog

### July 2017 (0.7.2)
 * Model scale is now mantained when importing.
 * Fixed import dialog.
 * More backend improvements.

### July 2017 (0.7.1)
 * Added clipboard copy support.
   * Only works on Windows and Mac.
   * Newlines are duplicated. I have no idea how to fix this.
 * Indented HTML for code window
   * This has no effect on your user experience, only the backend.

### July 2017 (0.7.0)
 * Added color support when importing.
   * Materials will have a prefix 'nfm'
     * Names are currently fucked
 * Restored support for legacy frontL and backL materials
 * Added RubyMine project
   * Will probably not work for you
 * Disabled debug features

### Aug 2015 (0.6.0)
 * Added new materials
   * noOutline
   * far
   * near
 * Enabled debug features
 
### Jan 2013 (0.5.2)
 * Original version by Jim