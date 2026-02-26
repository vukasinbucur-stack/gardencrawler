# Garden-Crawler: Complete Bill of Materials

**Project:** 4x4 Portal Rocker-Bogie Autonomous Weeding Robot
**Designer:** vook
**Location:** Timis County, Romania
**Last Updated:** 2026-02-26

---

## Summary

| Category | Est. Cost (EUR) | Priority |
|----------|----------------|----------|
| Structural | €250-350 | Phase 1 |
| Power System | €120-180 | Phase 1 |
| Drivetrain | €80-150 | Phase 1 |
| Control/Computing | €100-150 | Phase 1 |
| Hardware/Fasteners | €50-80 | Phase 1 |
| **Total (V1.0)** | **€600-910** | |

---

## 1. Structural Subsystem

### 2020 Aluminum Extrusion Frame

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| 2020 extrusion | 10m | meters | 20x20mm V-slot or similar | €80-120 | Local/AliExpress |
| Corner brackets | 24 | pcs | Internal 90° for 2020 | €12 | AliExpress |
| Joining plates | 12 | pcs | 2020 flat plates (100mm) | €10 | AliExpress |
| T-nuts | 50 | pcs | M5 drop-in T-nuts for 2020 | €5 | AliExpress |
| Gusset plates | 8 | pcs | Steel 3mm custom cut (100x100mm) | €20 | Local laser cut |
| End caps | 20 | pcs | 2020 plastic end caps | €5 | AliExpress |

**Subtotal: €132-172**

### Wheels & Hubs

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| 12" ag wheels | 4 | pcs | 304mm lug tread, with hubs | €80-120 | Alibaba/AliExpress |
| Wheel hubs | 4 | pcs | If not included with wheels | €20 | AliExpress |
| Axle adapters | 4 | pcs | Motor shaft to wheel adapter | €15 | Custom/AliExpress |

**Subtotal: €115-155**

---

## 2. Power System

### Primary Battery

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| 6S LiPo battery | 1 | pcs | 22.2V, 4000-6000mAh, 30C+ | €40-70 | AliExpress/hobby shops |
| 6S BMS | 1 | pcs | 30A common port BMS | €12-18 | AliExpress |
| XT60 connectors | 4 | pairs | Battery standard | €3 | AliExpress |
| LiPo charger | 1 | pcs | 6S balance charger, 50W+ | €25-40 | AliExpress/local |

**Subtotal: €80-131**

### Power Distribution

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| 24V→5V buck converter | 1 | pcs | 5A output, wide input | €8-12 | AliExpress |
| 20A inline fuse holder | 2 | pcs | ATO/blade style | €4 | AliExpress/local |
| 20A fuses | 5 | pcs | Spare fuses | €3 | Local |
| Power switch | 1 | pcs | Main power, 30A+ | €5 | AliExpress |
| E-stop switch | 1 | pcs | Red mushroom head, NC contacts | €8-15 | AliExpress/local |

**Subtotal: €28-39**

### Power Wiring

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| 14AWG silicone wire | 5m | meters | Red, 50A strand | €8 | AliExpress |
| 14AWG silicone wire | 5m | meters | Black, 50A strand | €8 | AliExpress |
| Terminal blocks | 2 | pcs | 2-position, 30A | €3 | AliExpress |

**Subtotal: €19**

---

## 3. Drivetrain

### Motors (4x)

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| JGB37-520 motor | 4 | pcs | 12V/24V, 35kg.cm, with encoder | €16-28 | AliExpress (ASLONG) |
| Motor mounting brackets | 4 | pcs | 37mm motor bracket | €8 | AliExpress |

**Specs per motor:**
- Voltage: 24V (or 12V option)
- Torque: 30-35 kg.cm
- Speed: 30-200 RPM (choose based on wheel size)
- Encoder: Hall effect, 11-360 PPR, 6-wire
- Shaft: 6mm or 8mm D-type

**Subtotal: €24-36**

### Motor Drivers

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| BTS7960 driver | 2 | pcs | Dual 43A peak H-bridge | €10 | AliExpress |
| OR VNH5019 driver | 2 | pcs | Dual 12A continuous (better quality) | €24 | Mouser/Digi-Key |
| OR Cytron 10A | 2 | pcs | MDD10A or MDS40A | €30 | Local/AliExpress |

**Recommendation:** Start with BTS7960 for budget, upgrade to VNH5019/Cytron for production.

**Subtotal: €10-30**

### Motor Wiring

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| 18AWG wire | 10m | meters | Motor power (varied colors) | €8 | AliExpress |
| 22AWG wire | 10m | meters | Encoder signals (6 colors) | €5 | AliExpress |
| JST-XH connectors | 10 | pairs | 2.5mm for encoders | €4 | AliExpress |
| Heat shrink | 1 | set | Assorted sizes | €3 | AliExpress |

**Subtotal: €20**

---

## 4. Control & Computing

### Primary Computer

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| Raspberry Pi 5 | 1 | pcs | 4GB or 8GB RAM | €60-80 | eMAG/Dedeman/local |
| Micro SD card | 1 | pcs | 32GB+, Class 10/A1 | €8-15 | Local |
| RPi 5 power supply | 1 | pcs | 27W USB-C PD (5V 5A) | €12-20 | Local/AliExpress |
| RPi case | 1 | pcs | With cooling fan | €8-15 | AliExpress |

**Subtotal: €88-130**

### Control Interface

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| Breakout board | 1 | pcs | For GPIO protection (optional) | €5 | AliExpress |
| PWM driver | 1 | pcs | PCA9685 16-channel (if needed) | €5 | AliExpress |
| Status LEDs | 5 | pcs | Various colors + resistors | €2 | AliExpress |
| Push button | 2 | pcs | For manual control interface | €2 | AliExpress |

**Subtotal: €14**

### Vision (Future)

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| OAK-D camera | 1 | pcs | Spatial AI stereo camera | €150+ | Luxonis |
| Camera mount | 1 | pcs | Adjustable arm for bird's eye view | €10 | Custom/3D print |

**Subtotal: €160 (Phase 2)**

---

## 5. Hardware & Fasteners

### Structural Fasteners

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| M5 x 10mm bolts | 30 | pcs | Button head, for 2020 | €5 | Local/AliExpress |
| M5 x 20mm bolts | 30 | pcs | Button head, for 2020 | €5 | Local/AliExpress |
| M5 nylon nuts | 50 | pcs | Lock nuts for vibration | €5 | AliExpress |
| M5 washers | 50 | pcs | Flat washers | €3 | AliExpress |
| M8 x 20mm bolts | 16 | pcs | For wheel hubs/high stress | €4 | Local |
| M8 nuts | 20 | pcs | Nylon lock nuts | €3 | Local |
| M8 washers | 30 | pcs | Flat and lock washers | €3 | Local |

**Subtotal: €28**

### Assembly Hardware

| Item | Qty | Unit | Description | Est. Price | Source |
|------|-----|------|-------------|------------|--------|
| Cable ties | 100 | pcs | Various sizes | €3 | Local |
| Velcro straps | 5 | pcs | For battery/wiring management | €4 | Local |
| Adhesive foam tape | 1 | roll | For vibration damping | €3 | Local |
| Standoffs | 20 | pcs | M2.5/M3, various lengths | €3 | AliExpress |

**Subtotal: €13**

---

## 6. Tools (Not Included - Assumed Owned)

- Allen keys (hex) for 2020
- M5 and M8 wrenches/sockets
- Soldering iron
- Wire strippers
- Multimeter
- Drill (for gusset plates)

---

## Total Cost Breakdown by Phase

### Phase 0: Minimal Mover (2WD)
- 2x motors, 1x driver, minimal frame, RPi 5
- **Target: Under €150**
- See [PHASE0_BOM.md](./PHASE0_BOM.md)

### Phase 1: Full 4x4 Chassis (No Vision)
- Complete structural, power, drivetrain, control
- **Target: €450-650**

### Phase 2: Vision & Autonomy
- Add OAK-D camera, implement CV
- **Target: +€200-250**

### Phase 3: Weeding Tool
- Mechanical weeding mechanism
- **Target: +€100-150**

---

## Notes

1. **Pricing:** Estimates as of Feb 2026. AliExpress prices fluctuate heavily.
2. **Voltage:** 24V recommended for motors, 12V works but at half torque.
3. **Encoders:** JGB37-520 includes 6-wire Hall encoder - confirm before buying.
4. **Wheels:** 12" agricultural wheels with lug tread are ideal. Smaller robot wheels work for testing.
5. **Substitutions:** Most parts have AliExpress alternatives. Local buying is faster but 2-3x more expensive.

---

## Next Steps

1. Review and prioritize parts for Phase 0
2. Create supplier shortlist for Romania
3. Begin procurement once funding available
4. Consider 3D printing some non-critical parts to save cost
