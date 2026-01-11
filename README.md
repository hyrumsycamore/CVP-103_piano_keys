# CVP-103 Piano Key Models
![IMG_2840](https://github.com/user-attachments/assets/b449d093-4b2f-4006-9868-93f06eeb6aa7)
This repository contains STL files for 3D-printable replacement keys for the Yamaha Clavinova CVP-103.

# Included Keys:
 - C / F Key (Universal mold)  
 - D Key  
 - E Key  
 - G Key  
 - A Key  
# Not Included:
 - B Key  
 - Accidentals (Sharps/Flats)  
 - Highest and Lowest C Keys (The unique keys at the far ends of the board)  

# Installation & Maintenance
To install the piano keys, you need to take apart practically the entire piano, I'd recommend watching this video by Mark Somoso Music  
https://www.youtube.com/watch?v=NWI-tHZ_EUY  
**Locking Mechanism Guide**
  Unlike the original OEM keys, these STL files do not yet feature external markings for the locking mechanism. Use the following list to ensure correct orientation:  
  &nbsp;&nbsp;&nbsp;&nbsp;A Key -- Left Side  
  &nbsp;&nbsp;&nbsp;&nbsp;E Key -- Left Side  
  &nbsp;&nbsp;&nbsp;&nbsp;C / F -- Key Right Side  
  &nbsp;&nbsp;&nbsp;&nbsp;D Key -- Right Side  
  &nbsp;&nbsp;&nbsp;&nbsp;G Key -- Right Side  

# Compatibility & Keybed Specs
These models were designed specifically for the Yamaha GH (Graded Hammer) action. While they were tested on a Clavinova CVP-103, they are likely compatible with any Yamaha instrument that uses the same "GH" part numbers  (e.g., VU101002 for the C key).
This includes many popular models such as:  
**CLP Series:** 800 and 900 series, plus early 100 series (CLP-120, 150, etc.)  
**CVP Series:** 90 series, 100 series, and 200 series.  
**P-Series:** P-80, P-90, P-120, P-155.  
**Professional Synths:** Motif 8, ES8, XS8, and S90.  
&nbsp;&nbsp;&nbsp;&nbsp;**Note on Tolerances:** Because these keys rely on a "snug fit" with the original hooking mechanisms, your printer's calibration is key. If you are using a different model than the CVP-103, I recommend printing a single "C" key first to test the return action and height.  

# 3D Printing Guide for Yamaha GH Keys  
  Because these keys are mechanical parts subject to repeated stress (the "pounding" you mentioned), printing them correctly is just as important as the model itself. Here are the recommended settings based on the iterative testing of this project.  
  **1. Material Selection**  
  &nbsp;&nbsp;&nbsp;&nbsp;**Recommended: PETG or ABS.** These materials have better "creep" resistance and flexibility than PLA. Since the keys use a hooking mechanism that must slightly flex during installation, PLA may be too brittle and snap over time.  
  &nbsp;&nbsp;&nbsp;&nbsp;**Avoid: Resin (SLA).** While beautiful, standard resins are often too brittle for the high-impact nature of a "Graded Hammer" action.  
  **2. Orientation**  
  &nbsp;&nbsp;&nbsp;&nbsp;**Horizontal** (On its side): This is the strongest orientation. By printing the key on its side, the layer lines run the length of the key. This ensures that the stress from your fingers doesn't pull the layers apart (delamination).  
  &nbsp;&nbsp;&nbsp;&nbsp;**Vertical (Standing up):** Not recommended. While it provides the smoothest surface finish for your fingers, the hooking mechanism at the back will be very weak and prone to snapping along layer lines.  
  **3. Slicer Settings**  
  &nbsp;&nbsp;&nbsp;&nbsp;**Layer Height:** 0.15mm to 0.2mm. Using a smaller layer height will make the curved edges feel smoother under your fingers.  
  &nbsp;&nbsp;&nbsp;&nbsp;**Wall Count (Perimeters):** 3-4 walls. Most of the strength should come from the walls, not the infill.  
  &nbsp;&nbsp;&nbsp;&nbsp;**Infill: 20-30% Gyroid.** Gyroid provides equal strength in all directions, which is great for the mechanical vibration of a piano key.  
  &nbsp;&nbsp;&nbsp;&nbsp;**Supports: Required.** Because of the internal cavities and the hooking mechanism, you will need to enable supports. Use "Snug" or "Tree" supports for easier removal from the tight internal channels.  
  **4. Post-Processing**  
  &nbsp;&nbsp;&nbsp;&nbsp;**Sanding:** To get that "OEM feel," start with 400-grit sandpaper and work your way up to 1000 or 2000-grit (wet sanding).  
  &nbsp;&nbsp;&nbsp;&nbsp;**Lubrication:** When installing, apply a small amount of PTFE (Teflon) grease (like Super Lube) to the guide pins and the hooking mechanism. This prevents the plastic-on-plastic squeaking that often occurs with 3D-printed parts.  

# Future Enhancements & Engineering Roadmap  
While the current models are fully functional, there are several "Stage 2" engineering goals I’ve identified to bring these even closer to the OEM Yamaha experience.  

**1. Integrated Maintenance Indicators**  
The original Clavinova keys feature molded Orientation Indicators that point toward the locking mechanism.  
&nbsp;&nbsp;&nbsp;&nbsp;**The Goal:** Integrate a small debossed arrow or icon into the top of the internal frame.  
&nbsp;&nbsp;&nbsp;&nbsp;**The Benefit:** This would simplify the installation and lubrication process for future repairs, ensuring that even someone unfamiliar with the internal chassis can orient the keys correctly.  

**2. Advanced Weighting & Inertia Control**  
To truly mimic a professional Graded Hammer action, the keys need to be heavier in the bass and lighter in the treble. I am exploring three levels of implementation:  
 &nbsp;&nbsp;&nbsp;&nbsp;**Level 1** (The Simple Fix): Varying the Infill Percentage from 50% (Bass) down to 10% (Treble). This changes the static weight but does not fully solve the "feel" of the key's return.  
 &nbsp;&nbsp;&nbsp;&nbsp;**Level 2** (Front-Loading): Using Slicer Modifiers to increase the density specifically at the front of the key. This better approximates the Moment of Inertia required for a realistic strike.  
 &nbsp;&nbsp;&nbsp;&nbsp;**Level 3** (The Professional Solution): Designing Internal Cavities within the model to allow for a "mid-print pause." This would allow the user to drop in small metal weights (like steel nuts or lead shot) before the printer seals the chamber, perfectly replicating the heft of a real piano key.  

**3. Dynamic Damping (Bounce Pads)**  
The original keys utilize a small rubber "Bounce Pad" at the tip of the locking shaft. While its exact purpose is subtle, I suspect it serves as a vibration dampener to reduce mechanical noise and prevent long-term wear on the chassis.  
&nbsp;&nbsp;&nbsp;&nbsp;**The Goal:** Design a secondary, screw-in or snap-fit component.  
&nbsp;&nbsp;&nbsp;&nbsp;**The Implementation:** This part would be printed in a flexible filament like TPU or TPE. It would be a fascinating challenge in Multi-material design and assembly tolerances to ensure the pad stays secure during high-intensity play.  

# The Origin Story: Engineering Hubris vs. Reality
This project was born from a mix of necessity and academic hubris. Growing up, I was forced into piano lessons—a chore I eventually grew to love in middle school when "pounding the keys" became my primary stress reliever. After getting married and moving into a college apartment, I finally decided to invest in a piano of my own. I scoured the local resale market and found what I thought was a steal on a Yamaha Clavinova CVP-103. It turned out the "great deal" was due to 14 of the keys being completely shattered. My initial engineering instinct was simple: just use some glue. To my dismay, the plastic was irreparable, and OEM replacements on eBay were nearly $10 per key. At $140+ for a full set, the repair cost was approaching the value of the piano itself. Naturally, I decided to put my engineering brain to work and 3D print the replacements. Easier said than done.  

**The Prototyping Process: 3D Scanning**  
Lacking extensive 3D modeling experience at the time, I attempted a high-tech shortcut: I used the professional 3D scanning arm available to students at BYU. The process was fascinating—the arm tracks its exact spatial coordinates in conjunction with a rotating pedestal, using a laser measurement system to plot thousands of points in real-time. Watching the digital twin form on the screen as if from nowhere was incredible.  

**The Technical Hurdle: Physics vs. Lasers**  
However, the excitement faded as soon as I ported the model to my laptop. I quickly learned a hard lesson in optical metrology: lasers and reflective surfaces do not mix. Because the piano keys were made of a slightly reflective, polished plastic, the laser light from the scanner was scattering and bouncing inconsistently. This created massive amounts of "noise" in the data. Instead of a crisp, mechanical part, the resulting mesh was a lumpy, irregular disaster that lacked the tolerances required for the Clavinova’s action.  
<img width="1687" height="525" alt="Screenshot 2026-01-10 115332" src="https://github.com/user-attachments/assets/681ac6ed-cb62-4bff-a904-30f0a7c42b81" />
<img width="1627" height="630" alt="Screenshot 2026-01-10 115348" src="https://github.com/user-attachments/assets/b8f8fd49-c082-4f28-b76f-4752c005e1f6" />

**From High-Tech Scans to High-Precision Calipers**  
Realizing the scanner wouldn't save me, I pivoted to a more traditional engineering approach. I sat down with a pair of digital calipers and an original key, learning the hard way how to take truly accurate measurements of complex, organic plastic shapes.
I spent weeks in Fusion 360, moving past the basics to master advanced tools like fillets for curved ergonomic edges and complex sketches for the internal hooking mechanisms. The goal was to ensure a snug fit with the piano's original infrastructure—a task that required understanding not just the shape of the key, but how it interacted with the guide pins and leaf springs inside the chassis.

**he Iterative Grind**  
The "C" key was my trial by fire. I went through five full iterations of that single model, spending hours staring at failed prints to wrap my head around why they didn't work. One version wouldn't return properly; another had a hooking mechanism that was too brittle.
However, once I perfected the fundamental dimensions and tolerances for the C key, the "engineering breakthrough" happened. Because the Clavinova uses a shared architecture for its keybed, creating the D, E, G, and A keys became significantly easier, usually requiring only one or two iterations to reach a perfect fit.  

**------ Under the Hood ------**
The most rewarding part of the process was the final installation. To replace the keys, I had to completely disassemble the Clavinova, giving me a front-row seat to its inner workings. I spent a great deal of time identifying the various components—from the weighted hammer action to the contact sensors—figuring out exactly how Yamaha’s engineers had translated a physical strike into a digital signal.  

These files are the result of that journey from a "lumpy" scan to a fully functional, 3D-printed keyboard.
