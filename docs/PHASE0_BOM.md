# Garden-Crawler: Phase 0 Minimal Build

**Goal:** Get the robot moving with minimal investment
**Target Budget:** Under €150
**Timeline:** 2-3 weeks from order to first movement

---

## Phase 0 Concept

The Phase 0 build is a **2-wheel test platform** that validates:
1. Motor control via Raspberry Pi 5
2. Encoder reading for speed/position feedback
3. Basic PWM + direction control
4. Power distribution (24V → 5V logic)

**What Phase 0 IS:**
- A simple rectangular frame (2WD, front wheels driven)
- Rear wheels are casters or simple free-spinning
- Battery mounted directly to frame
- RPi 5 with basic Python control script
- Manual control via keyboard or simple buttons

**What Phase 0 is NOT:**
- Not the final rocker-bogie suspension
- Not autonomous (no camera yet)
- Not field-ready (soft soil handling comes later)

---

## Phase 0 BOM

### Structural (€35-50)

| Item | Qty | Description | Est. Price | Source |
|------|-----|-------------|------------|--------|
| 2020 extrusion | 2m | 20x20mm V-slot | €16-24 | AliExpress |
| Corner brackets | 8 | Internal 90° | €4 | AliExpress |
| T-nuts | 16 | M5 drop-in | €2 | AliExpress |
| Casters | 2 | 100mm swivel casters (rear) | €8 | AliExpress/local |
| Mounting plate | 1 | 2020 flat, electronics | €3 | AliExpress |

**Frame layout:** 500mm x 300mm simple rectangle

---

### Motors & Wheels (€30-45)

| Item | Qty | Description | Est. Price | Source |
|------|-----|-------------|------------|--------|
| JGB37-520 motors | 2 | 12V/24V with encoders | €8-14 | AliExpress (ASLONG) |
| Motor brackets | 2 | 37mm motor mount | €4 | AliExpress |
| Wheels | 2 | 120mm robot wheels (6mm bore) | €12-20 | AliExpress |
| Shaft couplers | 2 | Motor-to-wheel adapter | €4 | AliExpress |
 OR M6 set screws | 4 | If wheels have set screw hubs | €1 | Local |

**Wheel note:** For Phase 0 testing, simple robot wheels are fine. 12" ag wheels can wait for Phase 1.

---

### Motor Driver (€5-12)

| Item | Qty | Description | Est. Price | Source |
|------|-----|-------------|------------|--------|
| BTS7960 driver | 1 | 43A dual H-bridge | €5 | AliExpress |
| OR L298N | 2 | Basic 2A driver (cheaper) | €4 | AliExpress |
| OR TB6612FNG | 1 | 1.2A dual (better quality) | €4 | AliExpress |

**Recommendation:** Start with BTS7960 (€5) - handles current with margin

---

### Power System (€30-45)

| Item | Qty | Description | Est. Price | Source |
|------|-----|-------------|------------|--------|
| 6S LiPo | 1 | 22.2V, 3000-4000mAh | €25-35 | AliExpress |
| XT60 connectors | 2 | pairs (battery + charger) | €1.50 | AliExpress |
| 24V→5V buck | 1 | 3A minimum for Phase 0 | €4 | AliExpress |
| Fuse holder + fuse | 1 | 10A inline | €2 | AliExpress |

**Alternative:** Skip LiPo, use bench power supply or 3S x 2 in series temporarily (-€25)

---

### Control (€90-110)

| Item | Qty | Description | Est. Price | Source |
|------|-----|-------------|------------|--------|
| Raspberry Pi 5 | 1 | 4GB model (€60) or 8GB (€80) | €60-80 | eMAG/local |
| Micro SD card | 1 | 32GB, Class 10 | €8 | Local |
| USB-C power | 1 | 18W USB-C charger | €10 | Local |
| RPi case | 1 | Basic with fan | €5 | AliExpress |
| Jumper wires | 1 | M-M, M-F set | €3 | AliExpress |
| Breadboard | 1 | For prototyping | €2 | AliExpress |

---

### Wiring & Hardware (€10)

| Item | Qty | Description | Est. Price | Source |
|------|-----|-------------|------------|--------|
| 18AWG wire | 3m | Red/black for motors | €3 | AliExpress |
| 22AWG wire | 3m | Multi-color for encoders | €2 | AliExpress |
| Terminal block | 1 | 2-position | €1.50 | AliExpress |
| Cable ties | 20 | For wire management | €1 | Local |
| M5 hardware | set | Bolts, nuts for assembly | €2 | Local/AliExpress |

---

## Phase 0 Total

| Category | Min | Max |
|----------|-----|-----|
| Structural | €35 | €50 |
| Motors & Wheels | €30 | €45 |
| Motor Driver | €5 | €12 |
| Power | €30 | €45 |
| Control | €90 | €110 |
| Wiring/Hardware | €10 | €15 |
| **TOTAL** | **€200** | **€277** |

---

## Getting Under €150

To hit the €150 target, these cuts are needed:

### Option A: Bench Power Supply (-€30)
- Skip LiPo battery and charger
- Use bench supply or old laptop charger (19V works, reduced torque)
- Add LiPo in Phase 1
- **New total: ~€170-250**

### Option B: Skip Wheels, Use Existing (-€15)
- Mount motors to frame, let them spin free
- Test encoder reading without movement
- Add wheels once motors confirmed working
- **New total: ~€155-235**

### Option C: RPi 4 Instead (-€20)
- Use RPi 4 (€40-50 used) instead of RPi 5
- Still plenty capable for motor control
- Upgrade to RPi 5 for vision (Phase 2)
- **New total: ~€180-255**

### Option D: Combo (Realistic €150 Path)
- RPi 4 (used/new): -€20
- Bench power supply: -€30
- Cheaper 80mm wheels: -€8
- **Revised total: ~€142-220**

---

## Phase 0 Assembly Order

1. **Week 1: Order Parts**
   - Motors + driver from AliExpress (2 week shipping)
   - RPi and local parts from Romanian suppliers

2. **Week 2: Local Parts Arrive**
   - Build 2020 frame
   - Install RPi and test power
   - Write basic motor control script

3. **Week 3: Motors Arrive**
   - Mount motors
   - Wire motor driver
   - Test first movement!

---

## Software: Phase 0 Goals

Create a Python script that:
1. Initializes PWM on GPIO pins
2. Reads encoder pulses via interrupt
3. Converts encoder ticks to distance/speed
4. Implements simple P-loop for straight driving
5. Responds to keyboard input (WASD or arrows)

**No vision, no autonomy yet** - just prove we can make wheels turn and read feedback.

---

## Phase 0 → Phase 1 Transition

Once Phase 0 is working (robot moves straight when commanded):
1. Add second motor pair (4WD)
2. Build full rocker-bogie suspension
3. Upgrade to 12" agricultural wheels
4. Add proper battery and BMS
5. Prepare for Phase 2: Camera integration

---

## Recommended First Order

**For immediate testing (order this week from local):**
- [ ] RPi 5 or RPi 4 + SD card + power
- [ ] 2m 2020 + 8 corners + 16 T-nuts
- [ ] Jumper wires + breadboard
- [ ] M5 bolts and nuts

**Order from AliExpress (takes 2-3 weeks):**
- [ ] 2x JGB37-520 motors (search: "JGB37-520 encoder 24V")
- [ ] 2x motor brackets (search: "37mm motor bracket 2020")
- [ ] 1x BTS7960 driver (search: "BTS7960 43A")
- [ ] 2x robot wheels (search: "120mm robot wheel 6mm bore")
- [ ] 24V→5V buck converter (search: "LM2596 5V 3A")

---

## Success Criteria

Phase 0 is complete when:
- [ ] Robot frame is built and stable
- [ ] Motors spin in both directions via RPi command
- [ ] Encoder readings are accurate (count ticks when wheel turns)
- [ ] Robot drives ~1 meter reasonably straight
- [ ] Can stop on command

Once these are achieved, you're ready for Phase 1: Full 4x4 Chassis!
