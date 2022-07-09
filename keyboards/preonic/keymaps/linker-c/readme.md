Preonic
===

![Preonic](http://i.imgur.com/EDWQbB0.jpg)

A compact 50% (12x5) ortholinear keyboard kit made and sold by OLKB and Massdrop. [More info on qmk.fm](http://qmk.fm/preonic/)

Keyboard Maintainer: [Jack Humbert](https://github.com/jackhumbert)  
Hardware Supported: Preonic PCB rev1, rev2, rev3  
Hardware Availability: [OLKB.com](https://olkb.com/preonic/), [Massdrop](https://www.massdrop.com/buy/preonic-mechanical-keyboard?mode=guest_open)

Make example for this keyboard (after setting up your build environment):

    make preonic/rev2:default

Install examples:

    make preonic/rev2:default:dfu         # For Preonic rev1 or rev2
    make preonic/rev3:default:dfu-util    # For Preonic rev3

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).


===========================================================================================
What I have changed.

1) Tap Dnace
Added tap dance for layer change keys.  I experienced with using one shot key and it
didn't perform as desirable.  I ended up using tab dance and it simplified the coding a lot.

I needed to use one tab for the "return" key to dub as right shift due to the limited columns.
MOD_TAP is a build in modifier that helps solving it for me.

2) Per layer RGB lighting
It would be nice to have different led pattern when the layer is switched.  It helps minimizing mistakes
when using scaled down keyboards that requires layers.
All the examples I could find online use fixed LED patern/color on layers.  Base layer is more flexible.
But I wanted the ADJUST layer to be the same as base layer because I assigned Hue & Saturation keys on
the ADJUST (both RAISE & LOWER keys pressed) layer.  So it's crucial to use the base layer's untouched
LED pattern so I can see the LED being adjusted live.
I also fixed the left 4 LEDs when CAPS is enabled. 


