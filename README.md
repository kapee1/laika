# Laika

<!-- Replace with actual photo -->
![Laika keyboard](https://github.com/user-attachments/assets/placeholder)

### Build guide — *coming soon*

---

### Main features:

* Custom compact layout — 53 keys
* Waveshare RP2040-Zero MCU
* MX hotswap sockets — supports Cherry MX and compatible switches
* Split spacebar support (2× 3u)
* SMD 1N4148W diodes (SOD-123) — no through-hole soldering
* Two plate options: Standard and Extra
* Optional top weight for extra heft and feel
* VIAL / QMK firmware

---

### Layout:

<!-- Replace with actual layout image, e.g. from keyboard-layout-editor.com -->
![Layout](https://github.com/user-attachments/assets/placeholder-layout)

---

### Sizes:

| Parameter | Value |
|-----------|-------|
| PCB size  | 257.2 × 100.2 mm |
| Plate options | Standard, Extra |

---

## BOM:

| Part | Quantity |
|------|----------|
| Laika PCB | 1 |
| Laika Case Top | 1 |
| Laika Case Bottom | 1 |
| Laika Plate (Standard or Extra) | 1 |
| Top Weight (optional) | 1 |
| Battery Cover (optional) | 1 |
| Waveshare RP2040-Zero | 1 |
| 1N4148W SOD-123 Diodes | 53 |
| MX-compatible switches | 53 |
| MX hotswap sockets | 53 |
| Stabilizers (PCB-mount) | *see note* |
| M2 screws | *see build guide* |
| M2 inserts | *see build guide* |
| Rubber feet | 4 |

> **Stabilizers:** Required for all keys ≥ 2u. The split spacebar layout uses two 3u stabilizers.

---

## Files:

```
laika/
├── case/
│   ├── top.step                          # Top case
│   ├── bottom.step                       # Bottom case
│   ├── battery-cover.step                # Battery cover
│   ├── standart-plate.step               # Standard plate
│   ├── extra-plate.step                  # Extra plate
│   ├── top-weight (laika).step           # Top weight — "laika" text
│   └── top-weight (laika-the-keyboard).step  # Top weight — "laika the keyboard" text
├── laika-pcb/
│   ├── laika-pcb.kicad_pcb               # PCB layout (KiCad 10)
│   ├── laika-pcb.kicad_sch               # Schematic (KiCad 10)
│   ├── laika-pcb.kicad_pro               # KiCad project
│   └── Production files/
│       └── Laika PCB gerbers.zip         # Ready-to-order gerber files
└── plate-dxf/
    ├── standart-plate.dxf                # Standard plate for laser cutting / CNC
    └── extra-plate.dxf                   # Extra plate for laser cutting / CNC
```

---

## PCB manufacturing:

Send `laika-pcb/Production files/Laika PCB gerbers.zip` to your preferred PCB manufacturer (JLCPCB, PCBWay, etc.) with the following settings:

| Setting | Value |
|---------|-------|
| Layers | 2 |
| Thickness | 1.6 mm |
| Surface finish | HASL / ENIG |
| Color | your choice |

---

## Firmware:

Laika runs on **VIAL** (QMK fork with real-time key remapping — no flashing required for layout changes).

<!-- Add firmware link once available -->
> Firmware files and flashing instructions — *coming soon*

**Flashing (RP2040-Zero):**
1. Hold the BOOT button on the RP2040-Zero while connecting USB.
2. A drive named `RPI-RP2` will appear.
3. Drop the `.uf2` firmware file onto that drive.
4. The keyboard will reboot and be ready to use.

---

## License:

This project is released under the [CERN Open Hardware Licence Version 2 - Strongly Reciprocal (CERN-OHL-S v2)](https://ohwr.org/cern_ohl_s_v2.txt).

You are free to use, study, modify, and distribute the hardware designs, provided that any derivative works are released under the same license and give proper credit.

---

*Named after Laika — the first living creature to orbit Earth.*
