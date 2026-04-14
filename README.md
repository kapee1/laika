# Laika - 45%-ish v4n4g0n-inspired keyboard  

![Untitled](https://github.com/user-attachments/assets/f81c8a55-02ba-4c5f-8245-b44c9089d1cf)


### Build guide — *coming soon*

---

### Main features:

* Custom compact layout — 47 keys + half of number row
* Waveshare RP2040-Zero MCU
* MX hotswap
* Split spacebar support (2 × 3u or 1 x 6u)
* Two plate options: Standard and Extra (extra plate has enlarged stabilizers holes)
* Top mount with o-rings
* The two halves of the case and top weight are held together by magnets
* VIAL / QMK firmware

---

### Layout:

![laika](https://github.com/user-attachments/assets/21be6c17-021e-478e-86d0-d041be580dcc)


---

## BOM:

| Part | Quantity |
|------|----------|
| Laika PCB | 1 |
| Laika Case Top | 1 |
| Laika Case Bottom | 1 |
| Laika Plate (Standard or Extra) | 1 |
| Top Weight | 1 |
| Battery Cover (optional) | 1 |
| Waveshare RP2040-Zero | 1 |
| 1N4148W SOD-123 Diodes | 53 |
| MX-compatible switches | 53 |
| MX hotswap sockets | 53 |
| Stabilizers (PCB-mount) | 2x3u or 1x6u |
| M2 screws x 4 mm | 10 |
| M2 inserts OD:3.2, H:3 | 8 |
| Rubber feet 3M SJ5302 (8x8x2) | 4 |
| Magnets 5x3 | 14 |
| Magnets 5x1 | 4 |
| Silicone o-rings 5x2 | 8 |

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
    └── extra-plate.dxf                   # Extra plate with enlarged stabilizers cutouts / CNC
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

Laika runs on **VIAL** (QMK fork with real-time key remapping — no flashing required for layout changes.


https://github.com/vial-kb/vial-qmk/tree/vial/keyboards/laika

**Flashing (RP2040-Zero):**
1. Hold the BOOT button on the RP2040-Zero while connecting USB.
2. A drive named `RPI-RP2` will appear.
3. Drop the `.uf2` firmware file onto that drive.
4. The keyboard will reboot and be ready to use.

---

## What is tested?

| Part | Is tested? |
|---------|-------|
| Top | Changed since proto, untested ⚠️ |
| Bottom | Changed since proto, untested ⚠️ |
| Standart plate | ✅  |
| Extra plate | Untested ⚠️ |
| Top weight | ✅ |
| PCB | ✅ |
| Battery cover | ✅ |

---

## Photos of PC proto:
![photo_2025-12-08_20-37-53](https://github.com/user-attachments/assets/e1f9eb90-9e45-409e-bb1d-9cf40d02987f)
![photo_2025-11-13_11-15-49](https://github.com/user-attachments/assets/f5c2d1a5-79ce-4c52-b59b-242a51485869)

![photo_2025-11-13_11-15-49 (2)](https://github.com/user-attachments/assets/dda19241-c370-4d5d-925c-4ebb83afbf62)
![photo_2025-11-13_11-15-51](https://github.com/user-attachments/assets/98c08180-d9fd-45fa-88c0-a79bf265a11c)
<img width="2560" height="1919" alt="image" src="https://github.com/user-attachments/assets/bd626f41-ece2-4235-81b7-9ddff9c3d72f" />

---

*Named after Laika — the first living creature to orbit Earth.*
