# How to assemble an elephant42

This is the build guide (assembly manual) for the self-made keyboard kit [elephant42](https://illness072.booth.pm/items/1775017).

**Before assembling, please read and understand this build guide first, prepare materials, tools, etc., build the environment, and finally perform the actual assembly work.**

**If you don't understand something or it doesn't work, don't be disappointed and give up there. Try [contacting me](https://twitter.com/illness072/). I would like to make an effort to help as much as possible.**

It will be smooth if you can ask "what you are trying to do", "what you did", and "what is going on" in an easy-to-understand manner.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [How to assemble an elephant42](#how-to-assemble-an-elephant42)
- [Preparation](#preparation)
  - [Check the contents of the kit](#check-the-contents-of-the-kit)
  - [Procurement of necessary parts](#procurement-of-necessary-parts)
    - [Required](#required)
    - [Optional](#optional)
  - [Tool Preparations](#tool-preparations)
    - [Necessary Things](#necessary-things)
    - [Good Things to Have](#good-things-to-have)
    - [Useful for Shopping](#useful-for-shopping)
  - [(For beginners) Studying soldering](#for-beginners-studying-soldering)
  - [Confirmation of the entire assembly process](#confirmation-of-the-entire-assembly-process)
  - [QMK firmware Build environment](#qmk-firmware-build-environment)
    - [QMK Environment Construction Troubleshooting](#qmk-environment-construction-troubleshooting)
  - [Pro Micro's measures against baldness](#pro-micros-measures-against-baldness)
- [Assembly work](#assembly-work)
  - [(Optional) Enable OLED option in firmware](#optional-enable-oled-option-in-firmware)
  - [Writing QMK firmware](#writing-qmk-firmware)
    - [QMK Write Troubleshooting](#qmk-write-troubleshooting)
  - [Main board (PCB) partition](#main-board-pcb-partition)
    - [(Optional) Color the sides of the PCB](#optional-color-the-sides-of-the-pcb)
  - [Soldering Pro Micro and Conthru](#soldering-pro-micro-and-conthru)
  - [(Optional) Backlight / Underglow LED installation](#optional-backlight--underglow-led-installation)
    - [Installation of backlight LED](#installation-of-backlight-led)
    - [LED TEST method](#led-test-method)
    - [Installation of underglow LED](#installation-of-underglow-led)
    - [LED installation troubleshooting](#led-installation-troubleshooting)
  - [Installation of diode](#installation-of-diode)
  - [Installing the switch socket](#installing-the-switch-socket)
  - [Installation of TRRS jack and reset switch](#installation-of-trrs-jack-and-reset-switch)
  - [(Optional) OLED installation](#optional-oled-installation)
    - [Please note only the RC version](#please-note-only-the-rc-version)
  - [Operation check](#operation-check)
    - [Operation check Troubleshooting](#operation-check-troubleshooting)
    - [Flux Cleaning](#flux-cleaning)
  - [Screwed](#screwed)
  - [(Optional) Rejoice in completion](#optional-rejoice-in-completion)
- [Customize](#customize)
  - [Keymap customization](#keymap-customization)
  - [OLED customization](#oled-customization)
  - [Acrylic plate customization](#acrylic-plate-customization)
  - [3D printing of special case](#3d-printing-of-special-case)
- [Daily care](#daily-care)
  - [clean up](#clean-up)
  - [Firmware update](#firmware-update)
- [finally](#finally)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Preparation

## Check the contents of the kit

Check that the contents are not missing or damaged.

Each acrylic plate has protective paper on the front and back. You can peel it off immediately, but it is better not to peel it off until just before assembly so that it will not get fingerprints, dust or dirt.

| ![Board (PCB)](build-guide/item_pcb.jpeg) |![Top plate](build-guide/item_top_plate.jpeg) |![Middle plate](build-guide/item_middle_plate.jpeg) |![ Bottom plate](build-guide/item_bottom_plate.jpeg) |
|:-: |:-: |:-: |:-: |
| Main board (PCB) ... 1 sheet <br />*** 1**| Top plate ... 2 sheets <br /> (Thinner with smaller holes) | Middle plate ... 2 sheets < br /> (Thicker and larger hole) | Bottom plate ... 2 sheets |
|![ProMicro Protective Plate](build-guide/item_promicro_plate.jpeg) |![Diode](build-guide/item_diode.jpeg) |![PCC Socket for MX Compatible Switch](build-guide/item_mx_socket.jpeg) |![TRRS Jack](build-guide/item_trrs_jack.jpeg) |
| ProMicro protective plate ... 2 pieces <br />*** 2**| Diodes ... 44 pieces <br /> (2 spare pieces) | For MX compatible switches <br /> PCB sockets ... 42 Pieces | TRRS Jack ... 2 pieces |
|![Tact switch](build-guide/item_tact_switch.jpeg) |![Spacer (short)](build-guide/item_spacer_short.jpeg) |![Spacer (long)](build-guide/item_spacer_long.jpeg) |![Screw](build-guide/item_screw.jpeg) |
| Tact switch ... 2 pieces <br /> * Colors may vary | Spacer (short) ... 20 pieces | Spacer (long) ... 4 pieces | Screws ... 40 pieces |
|![Cushion rubber](build-guide/item_cushion_rubber.jpeg) ||||
| Cushion rubber ... 10 pieces ||||

* 1 ... From v1, the board color is white. There is no difference in how to assemble.

* 2 ... ProMicro protective plates include two 2mm thick ones with the elephant42 logo engraved and two 3mm thick ones, for a total of four. Please select according to your preference.

## Procurement of necessary parts

Buy what you need but not included in the kit.

Please refer to the link of the recommended purchase destination (domestic mail order) for beginners.

### Required

- **Pro Micro (with conthrough) ... 2 pairs**
   - Recommended purchase destination
     - [Pro Micro (with conthrough) | Yusha Kobo](https://yushakobo.jp/shop/promicro-spring-pinheader/) * Please purchase two
     - TALP KEYBOARD
       - [Pro Micro ATmega32U4 5V/16MHz/MicroUSB2 (compatible product)](https://talpkeyboard.stores.jp/items/5b24504ba6e6ee7ec60063e3) * Please purchase two
       - [MAC8 Conthru XB-3-2.5-12P (Height 2.5mm/12 pins/1 piece)](https://talpkeyboard.stores.jp/items/5e056626d790db16e2889233) * Please purchase 4
     - Very cheap Pro Micro is sold as a set on Amazon etc., but it is safer to buy it at a proper store because you will get a bad product with a good probability.
   - Many domestic kits are included, but this kit is not included.
- MX compatible switches ... 42
   - Recommended purchase destination
     - [Switches | Yusha Kobo](https://yushakobo.jp/product-category/switches/)
     - [TALP KEYBOARD](https://talpkeyboard.stores.jp/?category_id=59cf8860ed05e668db003f5d)
     - [SWITCHES --Yukari Keyboard Factory](https://eucalyn.shop/product-category/keyswitches)
   --Please note that "Kailh Low Profile (Choc) Switch" and "Kailh Mid-Height Switch" are not supported.
- 1U keycap ... 42 pieces
   - Recommended purchase destination
     - [Keycaps | Yusha Kobo](https://yushakobo.jp/product-category/keycaps/)
     - [TALP KEYBOARD](https://talpkeyboard.stores.jp/?category_id=59be183f428f2d49120007b1)
     - [KEYCAPS --Yukari Keyboard Factory](https://eucalyn.shop/product-category/keycaps)
     - [Tai-Hao shop](https://shop.tai-hao.com/) * Overseas
     - [Rice keycap self-made keycap kit --Rabbit Goya --BOOTH](https://booth.pm/ja/items/1783747)
   - Please note that the keycaps for "Kailh low profile (Choc) switches" are not supported as well as the key switches.
- TRS cable ... 1
    - Also called an AUX cable or stereo mini plug cable. It is a cable with so-called earphone plugs attached to both.
      - Good-looking and cheap items are sold on Amazon etc.
    - The elephant42 requires a 3-pole (type with 2 black wires) TRS cable, but you can also use a 4-pole (type with 3 black wires) TRRS cable that is often sold at homebrew keyboard shops. It can be substituted.
      - [TRRS Cable 1m | Yusha Kobo](https://yushakobo.jp/shop/trrs_cable/)
      - [Self-made cable kit | Yusha Kobo](https://yushakobo.jp/shop/self-made-cable/)
      - [Transparent cable --Rabbit Goya --BOOTH](https://illness072.booth.pm/items/2227567)
- USB cable (Type-A to Micro-B) ... 1
    - It is a so-called Micro USB cable.
      - Good-looking items are sold on Amazon etc.
      - [USB Cable Micro B 1m | Yusha Kobo](https://yushakobo.jp/shop/usb_cable_micro_b/)
      - [Self-made cable kit | Yusha Kobo](https://yushakobo.jp/shop/self-made-cable/)
      - [USB2.0 cable (0.6m/USB (A) male--USB (Micro-B) male) | TALP KEYBOARD](https://talpkeyboard.stores.jp/items/5df82904a551d528d7360c34)


### Optional

1. OLED module (with pin socket) ... 2 pcs
    - [OLED module | Yusha Kobo](https://yushakobo.jp/shop/oled/) * Please select with pin socket
1. YS-SK6812MINI-E ... 54 pieces
    - [YS-SK6812MINI-E (10 pieces) | Yusha Kobo](https://yushakobo.jp/shop/ys-sk6812mini-e/) * Please purchase 6 packs (6 pieces left)
    - **The conventional product "[SK6812MINI](https://yushakobo.jp/shop/sk6812mini-35/)" cannot be used because it is not compatible.**
    - *** When purchasing at the Yusha Kobo actual store, do not accidentally purchase "[Reverse Mount RGB LED](https://yushakobo.jp/shop/a0800rl-10/)" which looks very similar. be careful. It cannot be used because it is not compatible.**


## Tool Preparations

Tools are required not only for assembly but also for repairs. Also, especially in electronic work, using good tools makes the work much easier.
It's a good idea to consult with your wallet and get the best tools possible.

Also, if there is a work space in a place that is easily accessible from home, you may want to consider using that space.

### Necessary Things

- Solder
  - [Goot High Density Integrated Substrate Solder SD-60](https://www.amazon.co.jp//dp/B0029LGAJI/)
    --Most parts are installed here
  - [Kutomi Denki Sangyo SH-43 Cryogenic Solder](https://www.sengoku.co.jp/mod/sgk_cart/detail.php?code=6A2W-CFJP)
    --Only the LED (YS-SK6812mini-E) has a risk of breaking at high temperatures, so I am using this just in case.
- Soldering wire
  - [goot solder blotting wire CP-3015](https://www.amazon.co.jp/dp/B001PR1KPQ)
- Soldering iron
  - [White light dial type temperature control soldering iron FX600](https://www.amazon.co.jp/dp/B006MQD7M4)
  -**We strongly recommend that you have a temperature control function**
- Iron stand
  - [HAKKO trowel stand 633-01](https://www.amazon.co.jp/dp/B000TGNWCS)
- flux
  - [goot PCB Flux BS-75B](https://www.amazon.co.jp/dp/B004ANR7KY/)
  - I sometimes see people who say that they can do it without it, but they are almost certainly advanced people who want to brag about their skills. Especially when you turn on the LED, please think that it is almost indispensable.
- Flux cleaner
  - [Tayo Denki Sangyo (goot) Flux Remover BS-T20B](https://www.amazon.co.jp/dp/B07JHJHTYG/)
  - It is not unnecessary if it is a non-cleaning type flux. It is brown and sticky and dirty, and it seems that it will damage the board due to aging, so please use it as much as possible.
- Kimwipe
  - [Nippon Paper Crecia Kim Wipe S-200 mini 62015 1 piece](https://www.amazon.co.jp/dp/B00CWA23P6)
  - Tissue can be used as a substitute, but I don't recommend it.
- Normal tweezers
  - Use the one purchased from Daiso. Shared with plastic model.
- Normal masking tape
  - Use the one purchased from Daiso. Shared with plastic model.
- Stick file
  - Use the one purchased from Daiso. Shared with plastic model.
- Ordinary utility knife
  - Anything is fine as long as it expires. This time, the design knife used in the plastic model is used instead.

### Good Things to Have

- Oil-based pen
  - Used to paint the side of the board. Please prepare your favorite color.
  - POSCA is recommended because of its good coloring. There is no problem with Gundam markers used in McKee and plastic models.
- Normal nippers
  - Use what you purchased at Daiso
  - It is recommended that you do not share good nippers for plastic models as they will damage the blade.
- Epoxy adhesive
  - Use what you purchased at Daiso
- Tester
  - I think it's better to have it, but I'm using a battery, an electronic buzzer, and a lead wire that are just loosely attached.
- Soldering work mat
  - I think it's better to have it, but I'm not using it
- Cutter mat
  - You can use old newspapers or the outer box of this kit as long as you don't damage your desk. This time I used the one used in the plastic model

### Useful for Shopping

Learn from your ancestors.

- [Tool memo required to make Helix keyboard kit | gist.github.com](https://gist.github.com/mtei/6957107a676ddfa85bde0ae41f8fa849)
- [8th "How to make your own keyboard #)
- [What you need to make your own keyboard | How to walk in the hot spring town](https://salicylic-acid3.hatenablog.com/entry/2018/11/24/%E8%87%AA%E4% BD% 9C% E3% 82% AD% E3% 83% BC% E3% 83% 9C% E3% 83% BC% E3% 83% 89% E3% 82% 92% E4% BD% 9C% E3% 82% 8B% E3% 81% 9F% E3% 82% 81% E3% 81% AB% E5% BF% 85% E8% A6% 81% E3% 81% AA% E3% 82% 82% E3% 81% AE #)
- [Tools used to assemble your own keyboard | yfuku blog](https://blog.yfuku.com/entry/keybord_build_tool)


## (For beginners) Studying soldering

The elephant42 will be soldered at a minimum of approximately 200 locations and a maximum of approximately 440 locations to complete.

Especially for those who are new to life or who haven't soldered in a long time since junior high school, it's a good idea to study how to solder.

If you skip here and start suddenly with the desire to complete it quickly, it will not fit in with you.**really.**


Basic operation of soldering

https://youtu.be/ZA-ehWjRfYM

Since the through holes are soldered when mounting ProMicro, tact switch, TRRS jack, etc., it is efficient to learn with this video.

https://youtu.be/oq3Q3n57-B0

It was efficient to learn how to solder surface mount diodes, LEDs, etc. in this video.

https://youtu.be/vqKKElJ1vw0


## Confirmation of the entire assembly process

The Daihuku Keyboiard channel made a great video, so please watch it and check the build !!

[! [I tried to make my own keyboard elephant42 edition | elephant42: Custom Mechanical Keyboard Build](https://img.youtube.com/vi/GmBnI3VYiT4/0.jpg)](https://www.youtube.com/watch) ? v = GmBnI3VYiT4)

By the way, it would be good to have a high rating and subscribe to the channel !!!!

## QMK firmware Build environment

Instructions for preparing the firmware can be found here.

https://docs.qmk.fm/#/ja/newbs_getting_started


Since elephant42 does not support QMK Configurator or QMK Toolbox, please build the build environment by referring to the above URL.

There is a place to execute `git clone --recurse-submodules https://github.com/qmk/qmk_firmware.git` on the way, but in the case of elephant42

```
git clone --recurse-submodules -b elephant42 https://github.com/illness072/qmk_firmware.git
```

Please.

Also, the part of `make <keyboard>: default` is

```
make elephant42: default
```

Please.


### QMK Environment Construction Troubleshooting

No matter how hard I try the above,**I can't build the environment**, I'm allergic to the command line,
If you have a situation where you can't use anything other than GUI, please see [here](via.md).

However, we would like to make this method**deprecated**for now, and only when using this method**we will not support**advice, answers to questions, etc.**.
Think of it as insurance when it just doesn't work.

## Pro Micro's measures against baldness


It's not required, but it's good because you won't feel sad if you do it.

Refer to the following articles, etc., and apply epoxy adhesive around the MicroUSB jack to strengthen the terminals.

- [Write QMK_Firmware while preventing moge of ProMicro](https://qiita.com/hdbx/items/2f3e4ddfcadda2a5578e)
- [Use masking tape to safely take measures against moge of ProMicro](https://cnaos.hatenablog.com/entry/2019/03/16/153754)



# Assembly work

## (Optional) Enable OLED option in firmware


**Please do this only when installing OLED. Enabling the OLED option in the firmware without the OLED installed can cause malfunctions.**

Open `keyboards/elephant42/rules.mk` of the QMK firmware` git clone` in the previous chapter with a text editor such as Notepad, and open it.

```
OLED_DRIVER_ENABLE = no # Enable / Disable OLED driver.
```

Modify the part that is as follows. (Change `no` to` yes`)

```
OLED_DRIVER_ENABLE = yes # Enable / Disable OLED driver.
```

Please save this and rebuild it.

```
make elephant42: default
```


## Writing QMK firmware

Plug the Micro USB cable into the Pro Micro, connect it to your PC, and then

```
make elephant42: default: flash
```

Then the writing will be executed. As the process progresses and you are ready to do the actual writing

```
Detecting USB port, reset your controller now ...
```

Is displayed, touch both RST and GND of the connected ProMicro at the same time with tweezers for a moment to short them.

The Pro Micro power light will then flash and the actual writing will begin.

When the following message is displayed at the end, writing is complete.

```
avrdude done. Thank you.
```

Do this for both the left and right Pro Micro.

**At this time, if you pull out the Pro Micro vigorously, the Micro USB jack will come off the board and become unusable. Take great care to pull it out slowly, gently and straight.**

|![Connect](build-guide/promicro_connect.jpeg) |![Firmware](build-guide/promicro_reset.jpeg) |
|-|-|
| Connect ProMicro to the PC and start the write command | When it is in the standby state, short the RST and GND for a moment to execute the write process |


### QMK Write Troubleshooting

In some environments, the following message may appear when executing a command. In this case, just press Enter and wait for a while, then wait for the write to fail and finish.

```
sh:/tmp/1: Permission denied
.override rw-r--r--root/wheel for/tmp/1? (Y/n [n])
```

If you get an error with the string `permission denied` like this,

```
sudo make elephant42: default: flash
```

I think that you can succeed by rewriting and executing. (You will be asked to enter the password, so enter the password for your account. At this time, the screen will not display anything like `**` or `●●●●`, but it will be It's normal, so don't worry, just enter your password and press Enter.)

## Main board (PCB) partition

Divide the PCB in two. Make a notch with a cutter along the perforation, slowly fold it by hand, and prepare the cross section with a stick file.

**Be careful not to scratch the rest of the board with the cutter.**
**When folding the board, hold it in the immediate vicinity of the target area and apply force so that other parts do not break or bend.**

|![Initial state](build-guide/pcb_first.jpeg) |![Make a notch](build-guide/pcb_cutter.jpeg) |
|:-: |:-: |
| Take out the PCB and place it on the cutter mat | Make a notch with the cutter along the perforations. <br/> Apply the blade dozens of times with a weak force so as not to damage other parts. |
|![Cut](build-guide/pcb_cutted.jpeg) |![Fold](build-guide/pcb_fold.jpeg) |
| Both sides, all four cuts have been made. | Fold it carefully so that other parts do not break or bend. <br/> If it is hard, do not try to fold it forcibly, and make a deep cut with a cutter. |
|![Broken](build-guide/pcb_broken.jpeg) |![Sandpaper](build-guide/pcb_sanding.jpeg) |
| Both sides broke cleanly. The small piece in the middle is unnecessary and should be thrown away. | The cut surface is jagged and dangerous, so clean it with a stick file. <br/> Since the powder will scatter during the sanding work, it is recommended that you do it in a place that is easy to clean and that you can get dirty. |
|![Yasuta](build-guide/pcb_sanded.jpeg) |
| It has become beautiful. If you trace the surroundings with your finger and it is flat, it is okay if you can see it with a slight vertical line. |


### (Optional) Color the sides of the PCB

As you can see in the picture, the side of the PCB has a strange color and looks bad, and it looks good even after completion, so it is recommended to paint it.

Trace the sides with an oil-based pen, and wipe off the ink on the front and back with a tissue or Kimwipe.

|![Paint color](build-guide/pcb_coloring.jpeg) |![Dry](build-guide/pcb_colored.jpeg) |
|:-: |:-: |
| Paint the sides of the PCB with a pen. Wipe it off immediately if it sticks out | If you work immediately after that, your hands will get dirty, so let it dry. |

It's common to paint with the same color as the PCB, but it's also nice to have an example of painting with a different color to accentuate it! Also, Pro Micro can be more complete by painting the sides in the same way.


## Soldering Pro Micro and Conthru

Check the orientation of the conthrough and insert it into the Pro Micro by referring to the photo.

It also fits into the main board (PCB) so that the ProMicro and Conslew are mounted at right angles, and then solder the Consul and ProMicro.

**Solder the ProMicro and the conthrough, not the main board (PCB) and the conthrough.**

After soldering the ProMicro and the conthru, remove the ProMicro (and the soldered conthru) from the main board once.


|![Consul](build-guide/konsuru.jpeg) |![Insert into Promicro](build-guide/promicro_konsuru_l.jpeg) |
|:-: |:-: |
| Consul has an orientation (windows open/not open). | Align the conthroughs and insert the ProMicro chip into the visible side. |
|![Opposite side](build-guide/promicro_konsuru_r.jpeg) |![Soldering](build-guide/promicro_solder.jpeg) |
| View from the opposite side. Make sure that the conthroughs are oriented in the same direction. | Fit it on the main board (PCB) and solder each pin from above. <br/> (I forgot to take a picture and took it later, so I have something other than ProMicro installed, but please do not see it.) |

It is recommended that you do not cut the legs of the conthrough that protrude from the top of the Pro Micro. The solder part was cracked (cracked), and my foot was completely pulled out from the other side.

## (Optional) Backlight / Underglow LED installation

Installing full-color LEDs is one of the most difficult tasks in the homebrew keyboard world, but with the advent of new LEDs, it has become much easier and safer to install.

Even if you have been frustrated before, why not try again this time?

### Installation of backlight LED

First, install only the backlight LED (left hand: L1 to L21, right hand: L29 to L49). Install a total of 42 pieces, 21 on each side.

If you use flux for soldering, you can easily, cleanly, and firmly bond.

The LED is a very small part, so it's a good idea to take it out and install it little by little so that you don't feel sad when you sprinkle it.

|![Temperature setting](build-guide/led_kote.jpeg) |![Place](build-guide/led_number.jpeg) |
|:-: |:-: |
| Setting the soldering iron temperature lower will greatly reduce the chance of the LED burning out. <br/> Check the melting point of the solder used and work at the lowest possible temperature. | Place the PCB face down (silver pad on top). |
|![LED mounting hole](build-guide/led_hole.jpeg) |![LED layout example](build-guide/led_hole_set.jpeg) |
| The LED is mounted in a square hole labeled Backlight or Underglow in white letters (silk). <br/>**Please install according to the installation number order written as L1, L2, ....**| LEDs are oriented. Place the Backlight downwards and the Underglow upwards. <br/> Also, there is a notch in only one of the four tabs extending from the LED, so make sure that tab is in the'G' position. <br/>**If the orientation is wrong, the LED will not light up, and in the worst case, the keyboard itself may break down. Please place it with the utmost care.**|
|![Backlight installation order](build-guide/led_number_bg.jpeg) |![Backlight installation example](build-guide/led_soldered_bg.jpeg) |
| As shown in the figure, attach from the thumb side to the little finger in the order of the white letters L1, L2 ... (silk) near the LED mounting holes. | I soldered L1. Make sure to visually check that the LED tabs are not floating from the board. |

### LED TEST method

If you install the LED, it will be smooth if you check the operation every time you install one to several LEDs.


The firmware for checking the operation of the LED can be written with the following command. Please write by referring to the procedure of [Write QMK firmware] (Write # qmk-firmware-) earlier.

```
make helix: led_test: flash
```

If you insert the ProMicro with this firmware burned into the PCB and connect it to the PC, it will light up in the order of "red → green → blue → red → ...".
You can check whether the soldering is successful by checking whether all the LEDs are lit correctly as "red → green → blue → red → ...".

When the PC is sleeping, it may only glow red and the color may not change.
Test when your PC isn't sleeping normally.

**It looks like it is being installed and tested in a good way**

|![1](build-guide/led_test_1.jpeg) |![2](build-guide/led_test_2.jpeg) |![3](build-guide/led_test_3.jpeg) |![4](build- guide/led_test_4.jpeg) |![5](build-guide/led_test_5.jpeg) |
|:-: |:-: |:-: |:-: |:-: |
| The backlight of the thumb shines | The index finger also shines | Then the middle finger and ring finger. A little more! | Little finger is complete. This completes the backlight! | Underground is OK. <br/> One-handed all done !! |

### Installation of underglow LED

Once the backlight LED installation is complete and all LED TESTs have passed, the underglow LED (left hand: L22 to L27, right hand: L50 to L55) can be installed. Install 12 on each side, 6 on each side.

|![Underglow installation order](build-guide/led_number_ug.jpeg) |![Underglow installation example](build-guide/led_soldered_ug.jpeg) |
|:-: |:-: |
| Next is Underglow. As with the backlight, install in the order of silk numbers. | I installed L27. Please note that the background and underglow are upside down. |


### LED installation troubleshooting

**The mounting holes are too tight to fit the LED**

This may happen due to manufacturing errors in board manufacturing. I intend to inspect it sufficiently, but I'm sorry for the omission.

In such a case, do not force it in, but scrape the inside of the LED hole a little with a stick file to widen the hole.

**Some LEDs do not glow**

It's likely that the non-lighting LED or the previous LED is wrong.

This article is about the previous version of SK6812MINI, not the YS-SK6812MINI-E used for elephant42.
The debugging method is described in detail in this article, so we recommend that you read it carefully.

[I made a cornet keyboard-I have a hard time installing LEDs- | Kiokuno Laundering](https://marksard.github.io/2018/08/04/make-the-crkbd/)

The pin assignment of YS-SK6812MINI-E is as follows, so it is different from that of SK6812MINI. Please read as appropriate.

|![LED pin assignment (front)](build-guide/led_f.jpeg) |![LED pin assignment (back)](build-guide/led_b.jpeg) |
|:-: |:-: |
| LED pin assignment (front) | LED pin assignment (back) |

**I made a mistake in installing the LED !!**

The important thing about fixing the LED is**don't rush to remove it**.

Basically, unless the LED itself is broken or misoriented, it often works just by reheating or re-soldering from above.

When removing parts, please be careful because if you do not do it carefully and well, the board will be easily damaged and in the worst case it may cause a catastrophe such as peeling of the land.

If the board is damaged, we also sell the board as a single unit, so please use that.

## Installation of diode

Install a total of 42 diodes, 21 on each side.**Please note that the diode is oriented.**

The diode is a very small part, so it's a good idea to take it out and install it little by little so that you don't feel dark when you sprinkle it.

|![Before installing diode](build-guide/diode_before.jpeg) |![After installing diode](build-guide/diode_soldered.jpeg) |
|:-: |:-: |
| `\ | ◁` Attach it where there is silk. Install so that the vertical line of the diode faces the side of `\ |` of `\ | ◁`. |

## Installing the switch socket

Install 21 switch sockets on each side, for a total of 42.**Please note that the socket is also oriented.**

The switch socket isn't a very small part, and it doesn't feel as painful to sprinkle it on, but it's still a good idea to take it out and install it little by little.

|![Before installing socket](build-guide/socket_soldered.jpeg) |![Notes on socket](build-guide/socket_attention.jpeg) |
|:-: |:-: |
| Install the socket. Please install according to the silk frame. | Be careful when mounting some diodes as they are very close to the mounting position. |

## Installation of TRRS jack and reset switch

Install one TRRS jack and one reset switch on each side.

**Turn the PCB over, fit it from the front side, then turn it over and solder the back side.**

The TRRS jack will fall off when turned inside out, so it's a good idea to secure it with masking tape.

|![Installation example](build-guide/trrs_switch.jpeg) |
|:-: |
| Insert the TRRS jack and switch from the front side, and solder from the back side.**Please note the front and back.**|

If you feel that the TRRS jack or reset switch that pops out of the PCB is too long, cut it a little with nippers to improve its appearance.

## (Optional) OLED installation

When installing an OLED, install the pin socket that came with the OLED.

This is also**fitted from the front side and soldered on the back side.**

The pin socket will fall off when turned inside out, so it's a good idea to fix it with masking tape.

|![Installation example](build-guide/oled_socket.jpeg) |![Done](build-guide/oled_soldered.jpeg) |
|:-: |:-: |
| Insert the pin socket from the front side and solder from the back side.**Please note the front and back.**| Insert the pin header into the pin socket, then insert the OLED and solder the OLED to the pin header. |

### Please note only the RC version

**The following issues have been fixed on the v1 board (white board). Please check only the RC version (red board).**

|![Caution for the first time](build-guide/oled_socket_rc.jpeg) |![Caution for the first time](build-guide/oled_socket_rc_2.jpeg) |
|:-: |:-: |
|**! Attention!**(I'm sorry ...) <br /> In the RC version (initial sale), the clearance between ProMicro and the pin socket is severe. <br/> Install ProMicro first, align the pin socket, and then install. | Also, the RC version (initial sale) has a slight OLED protrusion after completion. Please be assured that there is no problem in operation. |


## Operation check

At this point, all the soldering work has been completed. Let's check if the work so far is done well.

First, install the ProMicro and connect the TRS and USB cables.**Make sure to insert the USB cable on the left hand side.**

If you are burning the firmware for LED TEST with [LED TEST] (# led-test-method), refer to the procedure of [Write QMK firmware] (Write # qmk-firmware-) again to elephant42 firmware. Bake.

At this time, the procedure for short-circuiting GND and RST can be done simply by pressing the mounted reset switch. Also check the operation of the reset switch to see if it can be baked well.

After the connection is complete, use tweezers to short-circuit both sides of the switch socket and check if the switch is recognized as pressed.

In addition to opening a suitable text editor such as Notepad and confirming that the intended key is entered, you can also use the following test sites.

https://www.keyboardtester.com/

|![Install ProMicro](build-guide/test_start.jpeg) |![Short switch socket](build-guide/test_short.jpeg) |
|:-: |:-: |
| Install ProMicro from the front side, connect all cables, and burn the firmware again. <br/> When installing OLED, install OLED as well. | Short any key socket and see if the key behaves as if it were pressed.**Because you are touching from the back side, the left and right sides are reversed.**|
|![Default keymap (left)](build-guide/default_keymap_l.jpeg) |![Default keymap (right)](build-guide/default_keymap_r.jpeg) |
| The default keymap for the left hand. I think it's on the right side because it's turned inside out. | Right hand default keymap. I think it's on the left side because it's turned inside out. |

### Operation check Troubleshooting

**LED does not illuminate**

The behavior is correct as it shouldn't glow if you just burned the default farm.

Raise (right thumb, hold down second from inside) + c to turn the LED on/off.

**Only certain keys do not respond**

The key socket or diode may be defective in soldering, or the diode may be oriented in the opposite direction.

**Enter characters that a particular key did not intend**

There is a high possibility that something is short-circuited. Please check it carefully

**All specific rows and all specific columns do not respond**

Poor insertion of Pro Micro or defective soldering of the con-through is possible.

**All keys do not respond with both hands**

In particular, make sure that the ProMicro on your left is not missing or is installed upside down.

**All keys do not respond only on the right hand side (the one without USB inserted)**

Make sure that the ProMicro on the right hand side is not pulled out and that it is not installed upside down.

Alternatively, the TRS cable may not be fully inserted, or it may be defective.

**Behaves upside down**

First, be aware that you are looking at the keyboard from the back.

If that's the opposite, you're probably plugging the USB cable to your right hand (that is, to the left).

**Both left and right behave as left hand (or right hand)**

I don't really understand it, but it usually works.

1. Unplug the TRS cable and rehash both the left and right elephant42 farms.
2. Insert the TRS cable and re-burn the elephant42 farm with only your left hand.
3. Unplug and reinsert the USB cable

**The default keymap looks like it's for Mac, but I'm using Windows. .. ..**

I'm sorry, I don't have Windows and I haven't confirmed the operation.
The only difference between the two operating systems should be that Opt is treated as Alt and Cmd is treated as Win key.

**Other than that, or the above solution does not solve it**

I'm only worried if I can solve it, but for the time being, please [contact me] (https://twitter.com/illness072/). We will do our best to help you.

Let's do our best and be happy !!


### Flux Cleaning

Once the operation is confirmed, the soldering iron is no longer in play. Apply a flux cleaner and wipe it off with a Kimwipe.

When the board becomes shiny, the tension of the final assembly is different !!

## Screwed

Now, the completion is near.

Carefully peel off the protective paper from the acrylic plate and assemble it carefully to prevent dust, fingerprints and dirt from getting on it for a beautiful finish.

|![Installing ProMicro Protective Plate 1](build-guide/assemble_promicro_plate_1.jpeg) |![Installing ProMicro Protective Plate 2](build-guide/assemble_promicro_plate_2.jpeg) |
|:-: |:-: |
| Screw the spacer onto the ProMicro protective plate. <br/> Use the spacer (long) if the OLED is installed, and the spacer (short) if it is not installed. | In addition, screw the ProMicro protective plate + spacer to the board. |
|![Installing the top plate](build-guide/assemble_top_plate.jpeg) |![Installing the middle plate](build-guide/assemble_middle_plate.jpeg) |
| Screw the spacer (short) to the top plate. <br/>**Be careful not to get fingerprints !!**| Place the middle plate on it. <br/>**Be careful not to get dust in!**|
|![Installing the PCB](build-guide/assemble_pcb.jpeg) |![Installing the bottom plate](build-guide/assemble_bottom_plate.jpeg) |
| Add more PCB. | Finally, place the bottom plate and screw it in. |
|![Cushion rubber installation](build-guide/assemble_cushon_rubber.jpeg) |![Screwed completion](build-guide/assemble_complete.jpeg) |
| Paste the cushion rubber. | Turn it over and the keyboard itself is complete. |
|![Installing the keyswitch](build-guide/assemble_key_switch.jpeg) |![Installing the keycap](build-guide/assemble_keycap.jpeg) |
| Then attach your favorite key switch ... | Put on the key cap and you're done !! |

If you make both hands and connect the cables, you should have your own elephant42 in front of you. Congrats!!


## (Optional) Rejoice in completion

If you tremble with a sense of accomplishment and finish a small dance,
Why don't you take a picture of the completed elephant42 and upload it to Twitter? ([`# Elephant42`] (https://twitter.com/hashtag/elephant42) I would be very happy if you tweet with a hashtag. Please feel free to give us your opinions and impressions.)


# Customize

Well, the keyboard is complete, but this is just the beginning.

The real attraction of homebrew keyboards is their infinite customizability. Make your keyboard the best keyboard for you.

## Keymap customization

This is what the default keymap looks like, but I want to do this. Isn't it something like that?

You can customize the keymap to your liking by referring to these documents.

[Building the first firmware](https://docs.qmk.fm/#/ja/newbs_building_firmware)
[Edit QMK keymap for the first time](https://qiita.com/marksard/items/9317949ce1da327f7436)

## OLED customization

It's okay to put on OLED, but it's not good. And you who mourn. You can also display your favorite image.

There are many ways to do it, but I use this service. (It's a title like Helix only, but it can be used with elephant42 without any problem)

[I made a service to easily customize Helix's OLED display](https://qiita.com/guri3/items/844675b637c88515a989)

You can change the OLED display by replacing the created file with QMK's keyboards/elephant42/keymaps/default/glcdfont.c and building/writing the firmware.

## Acrylic plate customization

The elephant42 uses an acrylic plate called "Fluorescent Edge Pink", but you don't have to use pink at all.

You can use [Plate Cut Data](https://github.com/illness072/elephant42/tree/master/plates) to make an elephant42 of your favorite color using the acrylic cut service.

- [Laser processing service | Yusha Kobo](https://yushakobo.jp/shop/lasercut/)

## 3D printing of special case

We are also developing a [shining palm rest integrated case](https://github.com/illness072/elephant42/tree/master/cases/v1) exclusively for elephant42.

Try printing with your home 3D printer or various 3D printing services.

In addition, [plate cut data](https://github.com/illness072/elephant42/tree/master/plates) is also available, so I think it will be easier to challenge the completely original case design. .. (Please show me when you make it !!)


# Daily care

## clean up

Due to the fact that the acrylic plate is used as the material for elephant42, fingerprints due to hand grease and dust are liable to adhere due to static electricity.

If you are concerned, we recommend regular disassembly and cleaning with an antistatic cleaner for plastic/acrylic resin.

I often use something called "Acry Sunday Antistatic Cleaner Polycare F70".


## Firmware update

If it's working fine, you don't really need regular firmware updates, but if you want to try out the new features of QMK Configurator, you might want to try it. Familiarize yourself with `git` and try` pull`.

Also, the firmware of elephant42 is updated occasionally, such as changing the design of the OLED display. By all means if you are interested.


# finally

In writing this build guide, I would like to refer to [uzu42 build guide] (https://github.com/nrtkbb/Keyboards/blob/master/uzu42/build_guide_jp.md) by Naru (@nrtkbb). It was. Thank you so much.

The elephant42 is a keyboard that was very strongly influenced by the design philosophy of Fuku (@yfuku_)'s [claw44] (https://booth.pm/ja/items/1283873). It's a very good keyboard, so please try it if you like.