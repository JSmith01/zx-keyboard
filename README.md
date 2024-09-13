# Another (ZX/PC) keyboard case with Cherry MX switches


## Layout

4 were designed:
* `delta` reproduces classic ZX Spectrum+ / Delta-S clone keyboard

  ![Delta-S layout](https://github.com/JSmith01/zx-keyboard/blob/master/delta/delta-layout.png?raw=true)

* `next-like` follows ZX Spectrum Next quite closely, but uses standard third letter row shift of 0.5u instead of Next's non-standard 0.75u. Some other keys were swapped to keep it closer to the Spectrum+ layout.
  ![ZX Next-like layout](https://github.com/JSmith01/zx-keyboard/blob/master/next-like/zx-next-like-layout.png?raw=true)

* `13u` uses slightly condensed layout, requires only one stabilizer and only one stepped 1.25u key. Additionally it fits my 3d printer plate (256 mm square).

  ![13u condensed layout](https://github.com/JSmith01/zx-keyboard/blob/master/13u/13u-layout.png?raw=true)

* `13u-pc` PC-like keyboard to fit into 13u limit, requires 2 stabilizers, keycaps can be either printed or bought (however, some keys are barely of standard sizes).

  ![13u-pc condensed layout](https://github.com/JSmith01/zx-keyboard/blob/master/pc-58-key/58-layout.png?raw=true)


## Keycap models (Karon/Kopir-like)

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



## 13u wide keyboard case for a wedge case computer (WIP)

![RPi Zero 2 W wedge case computer](https://github.com/JSmith01/zx-keyboard/blob/master/pc-58-case/pictures/Image00005.jpg?raw=true)

![RPi Zero 2 W wedge case computer](https://github.com/JSmith01/zx-keyboard/blob/master/pc-58-case/case.png?raw=true)

Files for case parts are in `pc-58-case` directory. The main design constraint was, again, to fit each piece entirely into my 3d printer volume (cube of 256mm).

For my implementation I chose RPi 2 Zero W as a main board, mainly because of its low price and the fact I already had one. The design is parametric and it can be changed to adopt almost any board. The back cover of the case is a separate piece, so in case of re-printing it would require changing of the bottom piece and the back. The plate and the front keyboard case will remain unchanged. The case design is WIP still, however, I was able to print the plate, keycaps, and assemble it.

CAD link: https://cad.onshape.com/documents/80a6f71aa4ea5afbe3c2f400/w/0c9d95387bdbef7828758cf6/e/f104cb4e70454155592a95cd?renderMode=0&uiState=66de39ae955acf43bb4a916e

![RPi Zero 2 W wedge case computer](https://github.com/JSmith01/zx-keyboard/blob/master/pc-58-case/isometric-case.png?raw=true)

### 13u wide keyboard layout (PC like)

The directory `pc-58-key` has all the files for the layout, keycaps used, plate `.dxf` file. For the design, the only concerns were to fit into 13u limit, and have dedicated cursor keys (I hope it would help with retro gaming).

![RPi Zero 2 W wedge case computer](https://github.com/JSmith01/zx-keyboard/blob/master/pc-58-key/58-layout.png?raw=true)

It uses the same keycap models as ZX keys, but with other parameters:
* `#side_angle` (20 deg) 
* `#front_angle` (30 deg)
* `#rear_angle` (1 deg)

![58 keyboard 13u wide](https://github.com/JSmith01/zx-keyboard/blob/master/pc-58-key/58-keyboard.jpg?raw=true)

The keyboard needs 58 key switches (I used yellow gaterons), and 2 stabilizers - 2u and 4.5u (uncommon, but see below about using common 6.25u).


## Re-bending key stabilizers from 6.25u / 6.5u / 7u to 4.5u

Since I didn't find plate mounted stabilizers for 4.5u space, I had to bend the existing 6.25u stab to the needed dimension. This is a small guiding tool that helps to re-bend stab rod to the size of 4.5u. It requires two M2 screw bolts, 6-10mm long each. The model can be found in `auxilliary` directory.

![re-bend tool to 4.5u](https://github.com/JSmith01/zx-keyboard/blob/master/auxilliary/re-bend-4.5u.png?raw=true)

CAD link:
https://cad.onshape.com/documents/ae3792f91f504da8d6e72a6f/w/ced467ad9bcd54dddc1017f0/e/babc9538a75bcf5462f88daf?renderMode=0&uiState=66de3a5012896b37f23ab387
