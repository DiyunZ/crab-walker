# Crab Walker

A single-motor walking robot that picks up a payload, crosses grass, pebbles and hills, and drops it at the target. Built for ME 370 Mechanical Design I at the University of Illinois (Project Dawnstar II), spring 2026, by Team 12: Daniel Cai, Zac Vazquez, Shenbo Xue and Diyun Zheng.

<p>
<img src="media/cad-animation.gif" width="66%" alt="CAD animation of the Crab Walker walking">
<img src="media/walking-floor.gif" width="32%" alt="The built walker walking on the floor">
</p>

## The brief

- One motor and one degree of freedom for everything: walking, grabbing and releasing.
- Fit inside 18 x 18 x 30 cm in one configuration.
- Pick up a payload in the loading zone, carry it about 110 cm across the terrain of our choice, and drop it in the unloading zone, all within 15 minutes.
- $60 budget. We spent $56.30.

We chose the grass, pebbles and hills route. In the final evaluation the walker completed the mission and also cleared the steeper hill and rocky routes.

<p>
<img src="media/test-grass-hill.jpg" width="49%" alt="Walker on the grass and hill section">
<img src="media/test-pebbles.jpg" width="49%" alt="Walker on pebbles">
</p>
<p>
<img src="media/test-gravel.jpg" width="49%" alt="Walker on gravel">
<img src="media/test-woodchips.jpg" width="49%" alt="Walker on wood chips">
</p>

## Design

### Legs: eight Klann linkages, four sets per side

The Klann linkage turns the motor's rotation into a walking step with no control electronics. Compared with the alternatives we looked at, it lifts the foot higher for obstacles, keeps the foot on the ground longer for traction, and does not lift the whole body every step, which keeps motor torque low.

<p>
<img src="media/klann-linkage-dimensions.png" width="49%" alt="Klann linkage link dimensions in millimetres">
<img src="media/klann-linkage-animation.gif" width="49%" alt="Animation of one Klann linkage cycle">
</p>

Each side carries four leg sets arranged with a 180 degree phase offset, so at least four feet touch the ground at all times. That is what keeps the payload level on loose or uneven terrain.

<p>
<img src="media/phase-offset-diagram.png" width="49%" alt="Two leg layers with a 180 degree phase offset">
<img src="media/walking-phases.png" width="49%" alt="Feet in contact during the two walking phases">
</p>

### Drive train

A single input gear drives every leg crank through D-shafts, with a 2:1 reduction for the legs. A dynamic force analysis of the linkage located the peak-torque crank angles and toggle positions, which set the gear ratio and confirmed the motor's power margin.

<p>
<img src="media/drive-gear-layout.png" width="49%" alt="Drive gear layout">
<img src="media/drive-gear-animation.gif" width="49%" alt="Animation of the gear train">
</p>
<p>
<img src="media/dfa-motor-torque.png" width="49%" alt="Motor torque over one cycle from the dynamic force analysis">
<img src="media/dfa-motor-power.png" width="49%" alt="Motor power split between external loads and link inertia">
</p>

### Payload scoop and drop-off gate, on the same shaft

A U-shaped scoop arm lifts the payload by its side fins. Its driving gear has teeth on only part of its circumference, so once the arm has thrown the payload onto the slope it disengages and cannot stall the train. The payload slides down to a gate held by rubber bands on a reel; a 1:5 reel drive winds the bands in as the walker advances and opens the gate at the unloading zone.

<p>
<img src="media/gripper-cad.png" width="32%" alt="Scoop arm CAD">
<img src="media/partial-gear.png" width="32%" alt="Partial gear that disengages after drop-off">
<img src="media/unloading-slope-gate.png" width="32%" alt="Slope and gate for unloading">
</p>

<img src="media/payload-gripper.jpg" width="49%" alt="Payload held by the scoop arm on the built walker">

## Fabrication

The frame, linkage layers and gears are laser-cut 1/8 inch acrylic; the feet, the payload parts and the scoop are 3D-printed PLA. Layers are stacked on M4 screws and spacers, gears are cut to the D-shaft profile, and joints use low-profile screws tapped into the acrylic.

<p>
<img src="media/laser-cut-sheet.jpg" width="32%" alt="Laser-cut acrylic sheet">
<img src="media/walker-three-quarter.jpg" width="66%" alt="Finished walker, three-quarter view">
</p>
<p>
<img src="media/walker-front.jpg" width="49%" alt="Finished walker, front view">
<img src="media/walker-top.jpg" width="49%" alt="Finished walker, top view">
</p>

## Drawings

<p>
<img src="drawings/exploded-full-assembly.png" width="32%" alt="Exploded view of the full assembly">
<img src="drawings/exploded-leg-set.png" width="32%" alt="Exploded view of one leg set">
<img src="drawings/exploded-dispensing-system.png" width="32%" alt="Exploded view of the dispensing system">
</p>

## Files

| Folder | Contents |
|---|---|
| `drawings/` | Exploded assembly drawings |
| `media/` | Photos, CAD renders and animations used above |

## Credits

Team 12, ME 370 spring 2026: Daniel Cai, Zac Vazquez, Shenbo Xue, Diyun Zheng. Course staff provided the modular power unit; everything else was designed and built by the team. Parts and manufacturing through the Jackson Innovation Studio at UIUC.
