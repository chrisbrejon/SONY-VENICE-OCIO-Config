# SONY-VENICE-OCIO-Config
Based on the [LUT & ART Files | Sony Cine](https://sonycine.com/resources/luts/) I have created a minimal OCIO config of SONY VENICE for full CG projects. This is **the SONY VENICE 2 Workflow** in its most minimalistic and simple form:
* Inputs (textures) are in "linear"
* Rendering and Nuke working space are also in "linear"
* View Transform is for Rec.1886 display

There is no need to go wide gamut or do anything complex to **craft beautiful images**. Enjoy!

# Image Examples
<p>
    <img ![hue_sweep_sony_venice] width="144" height="81" src="https://github.com/user-attachments/assets/b650442d-0d05-4caf-bcb2-7e05ebf16b41" >  
    <img ![photographic_scene_sony_venice] width="144" height="81" src="https://github.com/user-attachments/assets/2f6fddf3-5f5d-4ffc-9a87-a8ba56d02487" >
    <img ![light_sabers_sony_venice] width="144" height="81" src="https://github.com/user-attachments/assets/9dc2f307-292f-4ec1-8b75-a37738cf334d" >
    <img ![lego_sailors_sony_venice] width="144" height="81" src="https://github.com/user-attachments/assets/e6ac4876-1378-4eec-b3f1-7ede27323e25" >
    <img ![louise_concert_sony_venice] width="144" height="81" src="https://github.com/user-attachments/assets/90d0ae68-34d4-49b7-83c4-717e284c27f3" >
</p>

Original files (encoded in "linear-AP0") are available [here](https://www.dropbox.com/scl/fo/fhzx0bcwcjylek1oz7kjc/ACGfmi0EHeufVOQPZLvvk7w?rlkey=53cp61955hbns8x46j6cf8k55&e=1&dl=0).

# About the config
* Reference color space is XYZ which is the base of all colourimetry
* All matrixes have been generated using [colour-science](https://www.colour-science.org/apps/) with "CIE XYZ-D65 - Scene-referred" and "CAT02"
* "linear" stands for "linear_bt.709"
* "cineonlog_rec709" can be used for a matte-painting workflow in Photoshop
* "slog3_sgamut3cine" is the shaper space. It can be used for color timing and some operations (such as sharpen)
* Substance_painter roles were set following [this page](https://mrlixm.github.io/blog/substance-painter-color-management/)
* No inverse of the View Transform has been provided
* One may easily add several colorspaces or displays for HDR output if needed (such as "Rec2020_D65_PQ")

# Looks
* 36 looks from the [LUT & ART Files | Sony Cine](https://sonycine.com/resources/luts/) have been added to the config
* **BUT** each of them has been merged with the SONY VENICE View in a single LUT
* I have set the "SONY VENICE High Contrast" to be the default View in the config
* To use one a different look, you need to switch it with the one I set by default. Like this for instance:

```active_views: [SONY VENICE DD01 Classic FPE, Un-tone-mapped, Log, Raw]```

# Other available Color Management Workflows
| Name                                                                                             | Author               | Release date |              Observations                             |
|:---:                                                                                             |         :---:        |      :---:   |                 :---:                                 |
| [ARRI K1S1](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator)     | Harald Brendel       | 2011         | THE most used LUT on the planet (ARRI Alexa workflow) |
| [ACES](https://github.com/AcademySoftwareFoundation/OpenColorIO-Config-ACES/releases)            | AMPAS                | 2016         | Color Encoding System developed by the Academy |
| [Filmic](https://github.com/sobotka/filmic-blender)                                              | Troy Sobotka         | 2017         | Original Blender Color Management used on [this movie](https://www.youtube.com/watch?v=uf3ALGKgpGU) |
| [RED IPP2](https://support.red.com/hc/en-us/articles/360041467533-RED-LUT-Downloads)             | Graeme Natress       | 2017         | RED Image Processing Pipeline explained [here](https://www.red.com/red-tech/image-processing-pipeline-ipp2) |
| [ARRI Reveal](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator)   | Sean Cooper          | 2022         | The new ARRI Alexa35 workflow described [here](https://www.youtube.com/watch?v=s_RXjVeC_7s) |
| [Tony](https://github.com/h3r2tic/tony-mc-mapface)                                     | Tomasz Stachowiak    | 2023         | A cool-headed display transform |
| [AgX Blender](https://github.com/EaryChow/AgX)                                                   | Eary Chow            | 2023         | Blender Color Management used on [this video game](https://www.youtube.com/watch?v=mVjBRZqajYY) |
| [TCAMv3](https://www.filmlight.ltd.uk/support/customer-login/colourspaces/colourspaces.php)      | Daniele Siragusano   | 2024         | Baselight Color Management Workflow explained [here](https://youtu.be/DL4n6LErMbw?t=325) |
| [AgX SB2383](https://github.com/sobotka/SB2383-Configuration)                                    | Troy Sobotka         | 2024         | Minimal AgX OCIO Config using Linear BT.709 |
| [JP-2499](https://github.com/jedypod/JP2499)                                                     | JP Zambrano          | 2024         | A popular picture formation pipeline described [here](https://www.liftgammagain.com/forum/index.php?threads/2499-drt-an-alternative-picture-formation-pipeline.18639/) |
| [Open DRT](https://github.com/jedypod/open-display-transform)                                    | Jed Smith            | 2024         | State-of-the-art Color Management Workflow |
