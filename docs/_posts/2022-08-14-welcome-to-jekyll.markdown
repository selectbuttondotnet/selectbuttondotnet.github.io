---
layout: post
title:  "Keyboards"
date:   2022-08-14 02:01:10 -0500
categories: jekyll update
---

**Layouts**

https://jhelvy.shinyapps.io/splitkbcompare/ offers comparison and scale diagrams of most split/ergo keyboards, including retail models like the Dygma Raise and ZSA Moonlander. Split/ergo keyboards are typically based on a 60% or 40% layout with different thumb clusters. Decide whether you want a number row and then find a thumb cluster that's comfortable for you to reach. Layouts are typically described as one half's rows x columns without the thumb cluster, e.g. a Lily58 is a 4x6 layout with thumb cluster.

There are generally two categories of split/ergo boards: retail designs like the Ergodox EZ, Dygma Raise, or ZSA Moonlander, and DIY designs like the Iris, Lily58, and Corne. 
- Retail designs are typically about twice as much as a DIY design but include niceties such as injection molded cases, more polished software tools such as Oryx https://configure.ergodox-ez.com/ for firmware customization, and more professional customer support. 
- DIY designs typically use either 3D printed or "sandwich" layer cases cut from acrylic or wood, may require setting up a *nix environment to compile and flash firmware, and may require you to join a Discord server to get support from the vendor or firmware community. You can typically order DIY designs partially assembled (i.e. with the soldering done) for a ~$75 fee.
- You may also consider other options including: non-MX switch support (e.g. Kailh Choc, ALPS, Mathias, etc.), rotary encoders, hotswap sockets for solderless switch changes, backlighting and underglow.

The app above has two notable exceptions: Kinesis*, the oldest ergo keyboard company, and Dactyl/Dactyl-derivative concave DIY designs. 

A Kinesis Advantage 2 is extremely comfortable because of its curved concave key "wells" where your hands can be almost completely relaxed. It's the best option if you have a serious RSI, type for a living, and want to coerce work to buy you something resembling a medical device. Kinesis also makes split keyboards with more traditional layouts like the Freestyle Edge and Freestyle Pro, which offer tenting and more relaxed shoulder positioning. But most of their products are poor by keyboard enthusiast standards because of their hollow acoustics, limited switch options, ABS keycaps with non-standard layout, and proprietary firmware. You can (and I have) modify a Kinesis board to address all of these issues, but I wouldn't start with one *unless* you need something "normal" to justify for HR.

Dactyl keyboards have curved concave wells like the Kinesis Advantage, but they're almost exclusively DIY with 3D printed cases and hand-wired matrixes. There are some limited run flexible PCBs for Dactyl designs but I'm not aware of any in stock at the moment. Ordering a Dactyl assembled is more akin to a commission than a retail assembly service and will run into hundreds of dollars and weeks of lead time. I am in the planning stages of a DIY Dactyl build but can't speak to them apart from the general caution above.

**Microcontrollers**

Most DIY designs use a Pro Micro MCU or a derivative design that adds features, though some like keeb.io's designs have integrated controllers on the PCB. 

The two most important derivative designs are the Elite-C, which replaces the Micro-USB with a USB-C port, and the nice!nano, which adds BLE support including between host/client boards.

Note: the nice!nano is not compatible with QMK, the predominant custom keyboard firmware, due to QMK's GNU license prohibiting proprietary bluetooth. You can use either BlueMicro or ZMK, the latter of which I have limited experience with. Read into these firmware options to make sure you're comfortable with the trade-offs and comparatively poor support/documentation before settling on wireless.

**Vendors**

I have purchased parts from all of the following vendors with no issues. I can't vouch for them and don't have relationships with any of them, but I have used them.

https://kbdfans.com/ (Chinese w/ huge inventory and fast but expensive shipping)
https://keeb.io/ (original designs e.g. Iris and Elite-C, cases, some pre-built)
https://boardsource.xyz/store (many PCB designs, cases, and build service)
https://www.littlekeyboards.com (many PCB designs and nice wood/acrylic cases but no build service)
https://novelkeys.xyz/ (original standard PCB designs and wide variety of switches)
https://www.us.txkeyboards.com/ (original films/springs)

I have also seen these recommended, but haven't used them personally.

https://keyhive.xyz/shop
[Clawboards](https://www.clawboards.xyz/shop)

I participated in a group buy through The Key Company and received all of the products I ordered, but they have had management and fulfillment issues since my order.

**Building**

Each keyboard should have a build guide typically hosted on the vendor's site or GitHub. e.g. https://docs.keeb.io/docs/iris-rev3-build-guide/, https://github.com/kata0510/Lily58/blob/master/Pro/Doc/buildguide_en.md

These should include a bill of parts and step-by-step instructions for assembly. If you can't find the build guide for the keyboard or it is poorly written, you may want to look at other options or reach out with your concerns if you're sold on the particular layout.

If you have difficulty during a build, asking the vendor or community on Discord is usually your best bet for advice.

**Soldering**

First, I'll defer to keeb.io and The Wirecutter for soldering supply recommendations.

https://docs.keeb.io/docs/soldering-tools/
https://www.nytimes.com/wirecutter/reviews/best-soldering-irons/

I can personally vouch for the YIHUA 939D+, but there are lots of options. A couple of points:

- If you are learning to solder, buy a breadboard to practice on, use leaded not-lead-free solder, and wear a mask so you're not inhaling the lead. 
- Through-hole soldering is much easier than surface-mount device (SMD) soldering. If you're inexperienced at SMD soldering, I recommend a through-hole PCB design like the Iris as opposed to the Lily58, or paying to have hotswap sockets installed by a vendor.

I recommend watching this Taeha Types video in which he builds two Keeb.io Iris boards for further examples. https://www.youtube.com/watch?v=0P6oIOB-whM

[details="Customizing Switches"]
There are three popular modifications to switches in the keyboard community: lubrication, springs, and films. 
- Lubrication can eliminate unwanted friction from the stem and contact leaf. 
- Lubricating and/or swapping springs with different materials and weight can eliminate noise and change the feel of a switch. 
- Filming a switch by placing a thin layer of plastic, vinyl, or silicone between the bottom and top of a housing can reduce play in the housing and change its sound.

For lubrication, these tutorials https://www.youtube.com/watch?v=44Wv4OGdmu4 https://www.youtube.com/watch?v=usNx1_d0HbQ by Taeha Types are a good primer. I've used Krytox 205g0 "grease" and Krytox GPL 105 "oil" for switches and springs respectively, and Super Lube dielectric grease for stabilizers on conventional keyboards. 

For springs, I've swapped springs in two keyboards to reduce the weight of Kailh Creams to a more standard 55g from 70g. I've used Novelkeys' and TX Springs, both of which had less "ping" than the stock Kailh springs. TX Springs offers a sample pack if you're experimenting with different weights.

I've had mixed success with films, but generally recommend Novelkeys and TX films if you're interested. I'd recommend a "site:reddit.com" search for your switch and films first to read reviews of applications.

Note: the above only applies for linear and tactile switches. Most people do not recommend lubricating clicky switches because lubrication can remove the sound and tactility without the benefits. You can lubricate the springs of clicky switches with no ill effects, but replacing springs on clicky and more pronounced tactile switches is tricky because a lower weight may not have enough force to properly rebound.

**Assembly Notes for DIY Boards**
- If you are installing switches in hotswap sockets in a DIY board, I highly recommend pressing on the plastic cover behind the socket so that the insertion force does not rip off the SMD pad. It is very difficult to repair a torn SMD pad on these PCBs.
- If your board uses a sandwich case, the pins on your switches and the friction between the switch housing and top plate are the only things holding your PCB in place. Make sure you get a good fit on each.

**Firmware**

If you bought a retail board, check with its documentation as it may have a GUI/web app tool for building firmware.

If you prefer a GUI and you're using a DIY board, you may be able to use QMK configurator https://config.qmk.fm/#/facew/LAYOUT_all or VIA https://caniusevia.com/ to most avoid CLIs provided your board supports it. Make sure you have the correct revision of your board and bear in mind some features like encoders and lighting may require building your own.

For setting up CLI environments, I'm going to link the documentation with an invitation to DM me because there's just too much to cover.
- I recommend setting up either of these build environments in a \*nix system rather than MSYS64 if you have a Mac or Linux environment available. It's just... plain easier.
- Keymaps are very flexible and easy to write in QMK, so don't be shy about looking around at others' on GitHub for ideas.

[QMK](https://beta.docs.qmk.fm/tutorial/newbs_getting_started)
[ZMK](https://zmkfirmware.dev/docs/)

**Re-Learning Touch Typing**

I adapted to the Kinesis Freestyle Edge with very few adjustments because the layout is essentially standard staggered but cut between the TGB and YHN keys. If your index fingers wander you may find this difficult, but it's a mild adjustment. (I *do* have strong feelings about how the number row is split -- 6 should go on the right hand, not the left. The Freestyle Edge breaks this but every other split/ergo board I know of does not.)

The Kinesis Advantage 2 required about a week to go from 40 wpm to 100 wpm due to the ortholinear columns. I had to unlearn bad habits like curling in my index finger to hit "c." I found https://www.keybr.com/ indispensable for this. It uses a type of spaced reptition study and algorithm to learn which keys and key combinations you have difficulty with and serve appropriate words both real and fake so you can't paper over technique with memorization.

After learning the Advantage 2, I found learning the Ergodox, Lily58, and Preonic layouts much easier and adjusted within hours of use. Don't be afraid to change the layout of modifier keys to suit your habits or logic. For example, I find left thumb to backspace and right thumb to space intuitive after learning the Advantage 2, so I overwrote the layout on the Lily58 to match. Most of these keyboards will require an embedded function row at a minimum, so learning to use QMK's layers is a huge ceiling on efficiency and economy.

* Trivia: Kinesis is responsible for the ubiquitous and now reviled Cherry MX Brown design, having requested a MX Blue derivative with quieter operation for offices in the 90s.