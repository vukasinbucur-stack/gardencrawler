# Garden-Crawler Project

## Project Overview
A modular autonomous agricultural robot designed as a helper around the farm. The bot uses an "aptitude + chore" architecture - each aptitude (e.g., weed/crop distinction) enables specific chores (e.g., weeding).

**Primary Mission (V1):** Weed/crop distinction and autonomous weeding in vegetable rows.

---

## Hardware Architecture

### Phase 0: Fixed Frame 2WD (Prototype)
- **Design:** Simple rectangular 2020 aluminum frame
- **Footprint:** 600mm (L) x 400mm (W)
- **Ground Clearance:** 150mm - sufficient for testing
- **Materials:** 30x30 aluminum extrusion
- **Wheels:** 80mm test wheels (upgraded to 12" agricultural for Phase 1)
- **Motors:** 2x JGB37-520 with hall encoders
- **Motor Driver:** VNH5019 dual driver
- **Computer:** Raspberry Pi 4

### V1.0: 4WD Field Robot (Future)
- **Chassis:** Fixed frame 4WD (suspension only if testing shows need)
- **Footprint:** 900mm (L) x 600mm (W)
- **Belly Clearance:** 300mm - allows straddling vegetable rows without damaging crops
- **Materials:** 2020 Aluminum Extrusion
- **Wheels:** 12-inch (304mm) lug-tread wheels for soft soil

### Electrical System
- **Primary Power:** 24V system (6S LiPo)
- **Logic Rail:** 5V/5A via Buck Converter for Raspberry Pi 5
- **Safety:** Physical E-Stop + 20A Inline Fuse
- **Motor Drivers:** VNH5019 (or Cytron for 4WD expansion)
- **Motors:** Planetary motors with quadrature encoders on all 4 wheels

### Brain & Vision
- **Primary Computer:** Raspberry Pi 5
- **Control:** PWM + Direction signals
- **Feedback:** Quadrature encoders for straight-line driving despite varying soil friction
- **Vision Platform:** Prepared for iPhone/OAK-D mount in "Bird's Eye" position

---

## Known Risks & Mitigations
1. **Motor synchronization** - Using encoder feedback to keep wheels aligned on varying soil friction
2. **Power delivery** - 24V system provides adequate torque for soft soil
3. **Wheel slip in mud** - Agricultural tires and weight distribution mitigate this
4. **Ground clearance** - 300mm belly clearance in V1.0 allows straddling crops

---

## Software Architecture

### Aptitudes (Capabilities)
- **Aptitude 1:** Weed/Crop Distinction (computer vision)
- Future: Disease detection, yield monitoring, soil analysis, pest detection

### Chores (Tasks)
- **Chore 1:** Autonomous Weeding
- Future: Precision spraying, navigation, data collection

---

## Developer Context
- **Name:** vook
- **Location:** Timis County, Western Romania
- **Profession:** Agronomist
- **Funding Strategy:** Blog content + consulting → EU grants (EAFRD, Horizon Europe)
- **Open Source Philosophy:** Making agri-tech accessible for small farms

---

## Code Priorities (In Order)
1. **Motor control + encoder feedback** - Get bot moving straight
2. **Camera vision pipeline** - Distinguish weeds from crops
3. **Autonomous navigation** - Follow rows, avoid obstacles
4. **Weeding logic** - Identify target, move to it, execute

---

## Current Status
- Design phase complete
- Cutting list/BOM being finalized
- Waiting on funding to begin procurement
- Blog/content strategy in development

---
