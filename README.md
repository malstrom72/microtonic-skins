Microtonic V3.3 Skinning Guide
==============================

Skinning support is limited in Microtonic V3.3, but it does support replacing image resources. 

The template folder contains all factory images for easier skin creation. Do not include factory images in your skin. If any resource file is missing in your skin folder, the built-in resource is used instead. 


Image formats
-------------
All image resources must be in PNG-8 (index palette), PNG-24 (RGB), or PNG-32 (RGBA) format.

Image dimensions are hardcoded into Microtonic and must remain the same. For animations or multi-state images, we use either frame strips or something we call pixel strips. 

Frame strips are images where each frame is stacked vertically. For example, a 100x100 pixel button animation with eight frames would be represented by a 100x800 pixel image.

Pixel strips are a proprietary format that we use on some images. In a pixel strip, each pixel from each frame is sequenced horizontally. By rearranging pixels this way, we can sometimes achieve higher file compression. We have a simple command-line utility to convert between frame strips and pixel strips that can be [downloaded here](https://soniccharge.com/forum/topic/1777).

All images in the Template have been converted to frame strips for easier editing.


Image Specifications
--------------------
```
aboutboxbackdrop_x2.png               940 x 760                 
aboutboxbubbles_x2.png                 64 x 2048     (  64 x 64  *  32 frames )
aboutboxoverlay_x2.png                900 x 720                 
background_x2.png                    1480 x 1100                 
beetleknob_x2.png                   12800 x 100      ( 100 x 100 * 128 frames )
bluetocyansquarebutton_x2.png         704 x 88       (  88 x 88  *   8 frames )
bluetogreenchannelbutton_x2.png      1184 x 60       ( 148 x 60  *   8 frames )
bluetogreenglasseggs_x2.png           800 x 100      ( 100 x 100 *   8 frames )
bluetogreensmalllanebutton.png        512 x 40       (  64 x 40  *   8 frames )
bluetoredsquarebutton_x2.png          704 x 88       (  88 x 88  *   8 frames )
buttonicons_x2.png                     48 x 336      (  48 x 48  *   7 frames )
cclabelbackground_x2.png              204 x 36       (  68 x 36  *   3 frames )
channelnotes_x2.png                    24 x 256      (  24 x 32  *   8 frames )
channeltitles_x2.png                   44 x 256      (  44 x 32  *   8 frames )
displaybuttons_x2.png                  48 x 120      (  48 x 60  *   2 frames )
displayfont_x2.png                     32 x 7200     (  32 x 32  * 225 frames )
horizontalbeetleslider_x2.png         100 x 60                  
icons_x2.png                           64 x 2112     (  64 x 64  *  33 frames )
inprintcharacters_x2.png               32 x 7168     (  32 x 32  * 224 frames )
matrixbackground_x2.png              1132 x 470                  
matrixchannels_x2.png                  60 x 414                  
matrixchoke_x2.png                     26 x 26                  
matrixnotes_x2.png                     56 x 1144     (  56 x 52  *  22 frames )
matrixplayposition_x2.png              58 x 8                 
matrixselection_x2.png               1088 x 50                  
menubutton_x2.png                      88 x 176      (  88 x 88  *   2 frames )
mididraghover_x2.png                   68 x 36                  
mididragicon_x2.png                    52 x 52                  
midilabelcharacters.png                12 x 240      (  12 x 12  *  20 frames )
midilabelcharacters_x2.png             24 x 480      (  24 x 24  *  20 frames )
midinotelabelbackground_x2.png         68 x 108      (  68 x 36  *   3 frames )
morphleds_x2.png                      768 x 24       (  24 x 24  *  32 frames )
patchdisplay_x2.png                   304 x 50                  
patterntitles_x2.png                   32 x 384      (  32 x 32  *  12 frames )
patterntitlesgray_x2.png               32 x 384      (  32 x 32  *  12 frames )
presetdisplay_x2.png                  568 x 50                  
programnumbers_x2.png                  20 x 416      (  20 x 32  *  13 frames )
smallmenubutton_x2.png                 76 x 152      (  76 x 76  *   2 frames )
tempo_x2.png                          250 x 26                  
verticalbeetleslider_x2.png            60 x 100                  
whitetobluechannelbutton_x2.png       148 x 480      ( 148 x 60  *   8 frames )
whitetoblueglasseggs_x2.png           800 x 100      ( 100 x 100 *   8 frames )
whitetobluelargeroundbutton_x2.png    800 x 100      ( 100 x 100 *   8 frames )
whitetobluematrixbutton_x2.png         60 x 480      (  60 x 60  *   8 frames )
whitetoblueroundbutton_x2.png         704 x 88       (  88 x 88  *   8 frames )
whitetobluesmalllanebutton_x2.png      64 x 320      (  64 x 40  *   8 frames )
whitetobluesquarebutton_x2.png        704 x 88       (  88 x 88  *   8 frames )
whitetogreenchannelbutton_x2.png      148 x 480      ( 148 x 60  *   8 frames )
whitetogreenroundbutton_x2.png         88 x 704      (  88 x 88  *   8 frames )
whitetogreensquarebutton_x2.png        88 x 704      (  88 x 88  *   8 frames )
whitetoredmutebutton_x2.png            60 x 480      (  60 x 60  *   8 frames )
```

Skin config file
----------------
Each skin has a corresponding `.mtskin` config text-file in the following format.
```
name: "Factory Template"
version: "1.0"
for: "3.3" 
by: "Fredrik Lidstr\xf6m"
url: "https://soniccharge.com"
thumbnail: "Template"
folder: "TemplateResources"
```
Thumbnail should be a PNG image in full GUI resolution (1440x1100)


Contributing
------------
Please follow standard GitHub procedures for contributing or updating your skin.
* Create a personal fork of this project.
* In your fork, create a new branch to work on.
* Add your skin in a new folder under `Microtonic Skins`.
* From your fork, open a pull request in the correct branch into this repository.