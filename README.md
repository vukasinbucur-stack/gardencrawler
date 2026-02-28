# Garden-Crawler

> An autonomous weeding robot for small farms.

Industrial weeding equipment costs €15,000+. Small farms can't afford this.
I'm building an open-source alternative for ~€600.

---

## Overview

Garden-Crawler is a 4x4 autonomous weeding robot designed for small-scale vegetable farms. It uses computer vision to distinguish weeds from crops and mechanical removal to eliminate them without herbicides.

**Target Cost:** €600
**License:** GPL-3.0 (see [LICENSE](LICENSE))
**Location:** Timis County, Romania

---

## Status

- [x] **Design Phase** — Complete
- [ ] **Phase 0** — Motor control testing (in progress)
- [ ] **Phase 1** — 4WD chassis construction
- [ ] **Phase 2** — Computer vision integration
- [ ] **Phase 3** — Field deployment

---

## Quick Specs

| Component | Specification |
|-----------|---------------|
| **Chassis** | 4x4 portal rocker-bogie, 2020 aluminum |
| **Motors** | 4x JGB37-520 planetary with encoders |
| **Driver** | VNH5019 dual H-bridge |
| **Brain** | Raspberry Pi 5 |
| **Vision** | OAK-D depth camera (planned) |
| **Power** | 6S LiPo (22.2V nominal) |
| **Belly Clearance** | 300mm (straddles crop rows) |
| **Footprint** | 900mm L × 600mm W |

---

## Documentation

Full build log, economics, and technical deep-dives:
**[gardencrawler.substack.com](https://gardencrawler.substack.com)**

### Quick Links

- [Bill of Materials](docs/BOM.md) — Complete parts list
- [Phase 0 BOM](docs/PHASE0_BOM.md) — Minimal starter build
- [Supplier Guide](docs/SUPPLIERS.md) — Sourcing options (Romania/EU)
- [Wiring Diagram](docs/wiring.md) — (coming soon)
- [Assembly Guide](docs/assembly.md) — (coming soon)

---

## Hardware

- **CAD Files:** [`cad/`](cad/) — Fusion 360 files, STL exports
- **Schematics:** [`hardware/`](hardware/) — KiCad, Fritzing diagrams
- **BOM:** [`docs/BOM.md`](docs/BOM.md) — Parts list with sources

---

## Firmware

- **Control Code:** [`firmware/`](firmware/) — Python motor control, encoder reading
- **Vision:** [`firmware/vision/`](firmware/vision/) — Weed/crop classification (planned)

---

## Contribute

This is an open-source project. Contributions welcome:

1. Fork the repo
2. Create a feature branch
3. Make your changes
4. Submit a pull request

Areas for contribution:
- Control algorithms (PID, path planning)
- Vision models (weed/crop datasets)
- CAD improvements
- Documentation fixes

---

## Sponsor

If this project helps you, consider **[sponsoring on GitHub](https://github.com/sponsors/vukasinbucur-stack)**.

All funds go directly to:
- Parts and materials
- Testing equipment
- Farm time for field validation

**Sponsor tiers:**
- €3/month — Early access to updates
- €10/month — Your name on the robot
- €25/month — Monthly consulting call

---

## About the Builder

Hi, I'm **vook**. I'm an agronomist in Timis County, Western Romania.

I grow vegetables, study weeds, and worry about the future of small farming. Industrial automation is priced for operations I'll never have. So I'm building my own — and sharing everything so others can do the same.

**Philosophy:** Agricultural knowledge should be free. If one farmer builds their own crawler because I shared mine, this project is a success.

---

## License

This project is open-source under **GPL-3.0**.

- Code: GPL-3.0
- Hardware designs: CERN-OHL-W or GPL-3.0
- Documentation: CC-BY-SA 4.0

See [LICENSE](LICENSE) for details.

---

## Acknowledgments

- Rocker-bogie design inspired by NASA's Mars rovers
- Open-source robotics community
- Romanian farming community

---

## Contact

- **Blog:** [gardencrawler.substack.com](https://gardencrawler.substack.com)
- **GitHub Issues:** [Use issues](../../issues) for bugs/questions
- **Email:** vukasin.bucur@gmail.com

---

*"Crawling toward better farming, one robot at a time."*
