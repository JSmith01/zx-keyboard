# Another ZX keyboard with Cherry MX switches


## Layout

3 were designed:
* `delta` reproduces classic ZX Spectrum+ / Delta-S clone keyboard

  ![Delta-S layout](https://github.com/JSmith01/zx-keyboard/blob/master/delta/delta-layout.png?raw=true)

* `next-like` follows ZX Spectrum Next quite closely, but uses standard third letter row shift of 0.5u instead of Next's non-standard 0.75u. Some other keys were swapped to keep it closer to the Spectrum+ layout.
  ![ZX Next-like layout](https://github.com/JSmith01/zx-keyboard/blob/master/next-like/zx-next-like-layout.png?raw=true)

* `13u` uses slightly condensed layout, requires only one stabilizer and only one stepped 1.25u key. Additionally it fits my 3d printer plate (256 mm square).

  ![13u condensed layout](https://github.com/JSmith01/zx-keyboard/blob/master/13u/13u-layout.png?raw=true)



## Keycap models

![ZX keyboard keys](https://github.com/JSmith01/zx-keyboard/blob/master/keycap%20models/keys.png?raw=true)

`.step` files are in `keycap models` directory, and the source can be found in the onshape CAD:

https://cad.onshape.com/documents/8eec099704dd56ee90a99779/w/f094e603417fd53c8f53642f/e/6200ad26f37156b8d2f7b3c0 (needs free account)

### Model params
* `#h_units` - 1u key only (horizontal units, supports 1-3u, 4.5u, 6.25u)
inside 1u key group - #stab_dist - formula to calculate distance between main key switch mount and stab mounts. Change it to support spacebars different from 4.5u/6.25u.
* `#side_angle` (25 deg) 
* `#front_angle` (35 deg)
* `#rear_angle` (5 deg)
* `#key_bend` (0.6mm) - amount of key surface bending, mm. 0.01mm is the minimum, also 4.5u automatically uses 0.01mm (flat surface for 3d printing)

All keycap parameters are set after Delta-S keyboard (Kopir / Karon factories), except the slightly bigger base key size. Here it is 18mm, common size for Cherry MX-based key switches, and on the real ZX keyboard it was 17.8 - 0.27mm according to factory blueprints (found an archive with it on the zx-pk.ru forum) - see `keycap blueprints` directory (all labels there are in Russian).

MX key spacebar stabilizer positions come from https://deskthority.net/wiki/Space_bar_dimensions

Other keycap dimensions are from https://blog.maxkeyboard.com/dwkb/keycap-profile-size-information/

Layout design service used: http://www.keyboard-layout-editor.com/
Plate generation service used: http://builder.swillkb.com/


## Keyboard case

TBD
