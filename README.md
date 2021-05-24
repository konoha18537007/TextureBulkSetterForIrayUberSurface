# Texture Bulk Setter For Iray Uber Surface
DAZ Studio Addon.

## Description
With this addon, you can set a set of PBR textures at once to the selected material(s) in the Sufaces Pane. By selecting just a single file in the GUI dialog, this addon sets the all of textures whose checkbox are checked, according to the pre-defined file name suffixes.

This addon is mainly useful for creating material presets.

![screen1](screen1.gif 'screen1')

As this script just skips the textures where missing files are specified, you don't need to bother unchecking the checkboxes for unused textures, just ignore.

You can change the suffix definition by editting settings.json.

The textures this script can handle and their suffixes by default are listed below.

| Texture | suffix |
| ------- | ------ |
| Base Color | [No Suffix] |
| Translucency Color | [No Suffix] |
| Glossy Reflectivity | _s |
| Dual Lobe Specular Reflectivity | _s |
| Diffuse Roughness | _r |
| Glossy Roughness | _r |
| Metallicity | _m |
| Base Bump | _b |
| Normal Map | _n |
| Displacement Strength | _h |
| Cutout Opacity | _o |

This script **only** supports **Iray Uber** shader.

I tested this only on DAZ Studio 4.15.0.2 Pro Public Build. Use this script at your own risk.

## Usage
1. Select the target object.

2. In the "Surfaces" Pane, select the target material(s) of the object.

3. Run this script. For example, you can run it by the either way below:
  * Drag and drop "texture_bulk_setter_for_iray_uber_surface.dsa" to the DAZ Viewport.
  * Double click the "texture_bulk_setter_for_iray_uber_surface.dsa" in content library.
    - You need to put this script in your library folder.

4. Click "Choose Base File..." and select a file whoes name is without any suffix.
  * This selection's result is only used for determining each texture file's path and names.

5. Tweak settings, if you want.
  * Uncheck check boxes at the left end which you don't want to use.
    - If the specified file dosen't exist, you don't need to uncheck it, because this script skips it whether unchecked or not.
  * If you want to specify some textures by your hand, push "Choose File..." and select it.

6. Push "Run" to set textures.

## Advanced Usage
You can change the suffixes and whether checked or not by dafault by editing settins.json.

* `enabled` key stands whether checked or not by dafault.
* `suffix` key stands the suffix.

## Installation
* Put this script anywhere you want.

## Unnstallation
* Delete this script.

## License
GPL-3.0 License 
