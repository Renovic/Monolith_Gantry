## FAQ
What does NP and FT mean?
- No Protrusion (NP) means the rear and front motors mounts don't protrude out of the frame perimeter
- Full Travel (FT) means the motor mounts protrude 4mm out of the frame, but it lets you get full travel (check configurator for distances)
- What should I pick?
 - If you want to stick with regular panels and don't need the overtravel, choose NP
 - If you want overtravel, pick FT, you will need either [Monolith Panels](https://github.com/Monolith3D/Monolith_Panels) or 4040 verticals to space out the panels

How much overtravel is there?
- Stock Voron: +10mm
- Monolith default config (spaced out panels or 4040): +13mm for all versions
- Monolith zero protrusion config (stock frame and panels):
 - VT 2WD: +9mm
 - VT AWD: +5mm
 - V2 2WD: +7mm
 - V2 AWD: +1mm
- X travel and front corner losses with AWD will be toolhead dependent.
- To switch between the two configs won't require the reprinting of motor mounts.

Should I choose printed or sheet metal?
- Both have rougly the same performance
- Sheet metal pulls heat away from motors and doesn't melt, letting you run higher motor currents or hotter chambers
- Sheet metal is more work

What are live shafts?
- Live shafts are where the 5mm shaft rotates with the pulley rather than the pulley idler rotating around the shaft
- F695 bearings can handle much higher loads than the small bearings in pulley idlers

What are dehubbed pulleys, and why are they necessary? 
- Dehubbed pulleys are regular pulleys but with their hub removed, and a new bottom flange inserted
- This is necessary for belts to pass through without rubbing 
<img width="1097" height="511" alt="image" src="https://github.com/user-attachments/assets/0c2dffe4-09ba-4466-a23e-b328fd4f5d03" />

Why do I need 2.5mm long grub screws?
- These need to be short enough to not rub on belts for dehubbed pulleys
- The max length is 2.7mm
- If you can't find 2.5mm grub screws you can either:
   - File down 3mm grub screws
   - Buy pressfit pulleys
   - Use retaining compound
 
What are long-shaft stepper motors?
- For 9mm belts, regular stepper shafts (24mm) aren't long enough to reach the double shear bearing
- For 6mm belts, regular steppers work in crazy ivan mode (up on one side, down on the other)
  - However, this does not work for front motor mounts on the trident because of the leadscrews intersecting with the motors
- Double shear is necessary to tension belts enough without bending the shaft
- Minimum for 9mm is 37mm (S37)
- Minimum for 6mm is 35mm (S35)
- Reccommended motors:
 - OMC 17HS19-2504S-H-V1
 - LDO 42STH48-2504AH (S55)
 - LDO-42STH48-2504AH (S45R)  - Monolith edition, with 2M long cables

What toolheads can I use?
- Monolith has a flipped belt path, so toolhead designs need to be designed with different belt clamps
   - Many toolheads make use of the [SLM Belt Clamp](https://github.com/Monolith3D/MISC/tree/main/Monolith_SLM_belt_clamps)
- Toolhead designs:
   - [Archetype](https://github.com/Armchair-Heavy-Industries/Archetype), with [Monolith Belt Clamps](https://github.com/Thescarecow/Archetype_Rail_Carriage_Clamp_Mod) (these are for Expiremental branch)
   - [Banantis](https://github.com/jakub874/Banantis)
   - [DK's Monolith Toolhead](https://github.com/Kizime123/DKs-Monolith-Toolhead)
   - [FiberSteam Toolhead](https://github.com/Shamoon78/Angry_Tool_Head/)
   - [FiberStream Toolhead](https://www.printables.com/model/1219174-fiberstream-toolhead)
   - [Gustav Railway Toolhead](https://github.com/RCI-Nicket/Gustav-Railway-Toolhead)
   - [Stormbreaker-Toolhead](https://github.com/Gr33n5murf/Stormbreaker-Toolhead)
   - [Takeoff-Toolhead](https://github.com/Kizime123/Takeoff-Toolhead)
   - [Trinity-Toolhead](https://github.com/WV-design/Trinity-toolhead/)
   - [UAP](https://www.printables.com/model/1353685-uap-v6)
   - [Xol-Toolhead](https://github.com/Armchair-Heavy-Industries/Xol-Toolhead), with [Monolith_Xol-Carriage](https://github.com/Armchair-Heavy-Industries/Armchair-Usermods/tree/main/files/Xol-Toolhead/Monolith_Xol-Carriage)
 
How do I assemble the XY joints?
<img width="1099" height="812" alt="image" src="https://github.com/user-attachments/assets/6d975dc8-8fa2-4cc9-8afb-4e36bc1cead4" />

What brackets should I use for the rear extrusion for Trident?
- In Full Travel (FT) mode, rotate the brackes 180 degrees
- In No Protrusion (NP) mod, use regular 2020 brackets

Is a 2020 frame enough?
- For 9mm AWD, upgrading the frame is important for achieving good IS graphs
- You can either upgrade to 4040 verticals or add [structural panels](https://github.com/Monolith3D/MISC/tree/main/Structural_Side_Panels_V2-VT)

What are these little tabs/slots for? (insert printed and sheet metal images)
 - They are for zipties to route your motor cables

How much should I tension my belts?
- [Belt tension Calculator (Lukes Lab)](https://www.lukeslabonline.com/pages/belt-tension-calculator)
- For large builds, the built-in tension range isn't enough, so you can use a pretensioner

Should I use gt3 belts?
- GT3 doesn't signficantly improve IS results, and requires significantly more tension to match GT2
- If you want to improve on belts, increasing belt size is more beneficial
- [Tests](https://monolith-gantry-updates.zen3d.eu/gt3-vs-gt2-epdm-belt-recommendation/)
