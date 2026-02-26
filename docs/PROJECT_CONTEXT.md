# Garden-Crawler Project

## Project Overview
A modular autonomous agricultural robot designed as a helper around the farm. The bot uses an "aptitude + chore" architecture - each aptitude (e.g., weed/crop distinction) enables specific chores (e.g., weeding).

**Primary Mission (V1):** Weed/crop distinction and autonomous weeding in vegetable rows.

---

## Hardware Architecture (V1.0)

### Chassis: 4x4 Portal Rocker-Bogie
- **Design:** Inverted arches with teeter-totter differential logic
- **Footprint:** 900mm (L) x 600mm (W)
- **Belly Clearance:** 300mm - allows straddling vegetable rows without damaging crops
- **Materials:** 2020 Aluminum Extrusion
- **Wheels:** 12-inch (304mm) lug-tread wheels for soft soil

### Electrical System
- **Primary Power:** 24V system (6S LiPo)
- **Logic Rail:** 5V/5A via Buck Converter for Raspberry Pi 5
- **Safety:** Physical E-Stop + 20A Inline Fuse
- **Motor Drivers:** Cytron motor drivers
- **Motors:** Planetary motors with quadrature encoders on all 4 wheels

### Brain & Vision
- **Primary Computer:** Raspberry Pi 5
- **Control:** PWM + Direction signals
- **Feedback:** Quadrature encoders for straight-line driving despite varying soil friction
- **Vision Platform:** Prepared for iPhone/OAK-D mount in "Bird's Eye" position

---

## Known Risks & Mitigations
1. **High Center of Gravity** - 24V batteries mounted low on rocker legs as counterweights
2. **Joint Stress** - Using external steel gusset plates for arch-to-chassis connections (upgraded from T-nuts)

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

## Conversations with Claude
- Previous brainstorming sessions covered financing strategy, EU grants, content/consulting approach
- Emphasis on building a working prototype first before seeking major funding
- Open-source documentation philosophy
