![Clean SL](img/Themes.gif)

# Labels #

Collection of Script Snippets and Label Themes for Adobe After Effects script [Labels](https://aescripts.com/labels/)

## How to ##

1. In the Labels interface click a button with text **S** (settings) and chose **Open Custom Shortcuts Editor**,
2. In the **key:** section assign a shortcut to be used, say `shift + m`, and select a snippet by clicking on `...` and navigating to a file,
3. Confirm changes by clicking on **Save Shortcuts for Scripts**,
4. Back in AE hold down the shortcut key you assigned in step #2 `shift + m`, and click on any label swatch in Labels interface - this will fire-up the script that is linked to this shortcut.


## Snippets ##

* [Copy Color To Clipboard](Snippets/Copy%20Color%20To%20Clipboard.js) - copies labels HEX color to the clipboard,
* [Create Shape Layer](Snippets/Create%20Shape%20Layer.js) - creates a full sized Shape Layer and sets Fill color to the label color,
* [Create Solid Layer](Snippets/Create%20Solid%20Layer.js) - creates a full sized Solid Layer and sets its source color to the label color,
* [Group Layers](Snippets/Group%20Layers.js) - groups all layers with same label color together underneath the topmost layer with that color,
* [Parent Layers to Null](Snippets/Parent%20Layers%20to%20Null.js) - parents all layers with the same label color to a null,
* [Push Layers Back By One](Snippets/Push%20Layers%20Back%20By%20One.js) - pushes layers with this label to the bottom of the layer stack one by one,
* [Push Layers Up By One](Snippets/Push%20Layers%20Up%20By%20One.js) - pushes layers with this label to the top of the layer stack one by one,
* [Shy Everything Except](Snippets/Shy%20Everything%20Except.js) toggles 'solo' property of all layers that do not match given label color in composition,
* [Toggle Shy](Snippets/Toggle%20Shy.js) - toggles 'shy' property of all layers with given label color in composition,
* [Toggle Solo](Snippets/Toggle%20Solo.js) - toggles 'shy' property of all layers with given label color in composition.

``` javascript
Labels script exposes following API:
    index (Number) label index,
    hex   (String) label HEX color,
    rgb   (Array)  label RGB color [0-255, 0-255, 0-255],
    name  (String) label name
```

``` javascript
// Assuming myLayer is a Layer Object in composition:


// Check if layer index matches Labels.index:
if (myLayer.index === Labels.index) {
    alert('Eureka!');
} // => 'Eureka!'


// Set layers comment to Labels.hex color:
myLayer.comment = Labels.hex;


// Create a Solid Layer with base color of Labels.rgb
// (assumes that myComposition is active Comp Item)
var myLayer = myComposition.layers.addSolid(
    Labels.rgb / 255,
    'My Layer',
    myComposition.width,
    myComposition.height,
    1
);


// Set layer name to Label.name
myLayer.name = Labels.name;
```

## Themes ##

* [David Arbor](https://www.davidarbor.com/) theme [![button](img/theme_david_arbor.png)](zip/Themes/David%20Arbor.theme.zip)
* Generic Color Game Palette v16 CGP by [Arne Niklas Jansson](http://androidarts.com/palette/16pal.htm) [![button](img/theme_generic_16_cgp.png)](zip/Themes/Generic%2016%20CGP.theme.zip)
* Material theme based on [Google Material Design](https://material.io) [![button](img/theme_material.png)](zip/Themes/Material.theme.zip)
* Colection of pastel colors [![button](img/theme_pastel.png)](zip/Themes/Pastel.theme.zip)
* [Paul Conigliaro](http://conigs.com) ( [@Conigs](https://twitter.com/conigs) ) theme [![button](img/theme_paul_conigliaro.png)](zip/Themes/Paul%20Conigliaro.theme.zip)
* Pico-8 Game Console Palette by [Lexaloffle](https://lexaloffle.com/pico-8.php) [![button](img/theme_pico8.png)](zip/Themes/Pico-8.theme.zip)
* [Ryan Summers](http://ryansummers.net) ( [@Oddernod](https://twitter.com/Oddernod) ) theme with custom Label Assignments [![button](img/theme_ryan_summers.png)](zip/Themes/Ryan%20Summers.theme.zip)
* Vivid, almost random colors with bold hues [![button](img/theme_vivid.png)](zip/Themes/Vivid.theme.zip)