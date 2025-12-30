# 🖥️ Distribución de Hardware por Módulo

## VISIÓN GENERAL
| Módulo Físico | Arduino Mega | Arduino Uno | Componentes Principales |
|---------------|--------------|-------------|-------------------------|
| FCU/EFIS/WARNING | MEGA 1 | - | 7 encoders, 18 botones, 5 displays |
| OVERHEAD PANEL | MEGA 2 | UNO 1 | 4 encoders, 13 toggles, 25 botones |
| PEDESTAL | MEGA 3 | UNO 2, UNO 3, UNO 4 | 14 encoders, 2 toggles, 35 botones |
| MCDU | MEGA 4 | - | 70 botones |

## DETALLE POR PLACA

### MEGA 1 - FCU/EFIS/WARNING
- **Encoders (7):** SPD, HDG, ALT, VS, ROSE, DISTANCIA, BARO
- **Botones (18):** SPD MACH, LOC, AP1, AP2, A/THR, EXPED, APPR, CSTR, WPT, VOR, NDB, ARPT, FD, LS, CHRONO, M WARN, M CAUT, AUTO LAND
- **Toggles (1):** ADF1/VOR1
- **Displays TM1637 (5):** SPD, HDG, ALT, VS, BARO
- **Pines utilizados:** ~51/70

### MEGA 2 - OVERHEAD (Encoders + Toggles)
- **Encoders (4):** Wiper, ADIR1, ADIR2, ADIR3
- **Toggles (13):** CAPT & PURS, STROBE, BEACON, WING, NAV & LOGO, RWY, LAND L, LAND R, NOSE, SEAT BELTS, NO SMOKING, EMER EXIT LT, DOME
- **Pines utilizados:** ~28/70

### UNO 1 - OVERHEAD (Botones)
- **Botones (19):** GND CTL, CREW SUPPLY, SYS, G/S MODE, FLAP MODE, LDG FLAP3, MASTER, START, PWH, WING, ENG1, ENG2, APU BLEED, BAT1, BAT2, EXT PWR, ENG1(FIRE), APU(FIRE), ENG2(FIRE)
- **Pines utilizados:** 19/20

### MEGA 3 - PEDESTAL (Encoders + Toggles)
- **Encoders (14):** PFD, ND, ATT HDG, AIR DATA, EIS DMC, ECAM, GAIN, WX, WX RADAR + 5 ATC
- **Toggles (2):** XFR (GPWS), SYS (RADAR)
- **Pines utilizados:** ~45/70

### UNO 2 - PEDESTAL (Botones parte 1)
- **Botones (17):** PULL UP, UNLK1, UNLK2, UNLK3, LO, MED, MAX, NUMBERS(1-9)
- **Pines utilizados:** 17/20

### UNO 3 - PEDESTAL (Botones parte 2 - ECAM)
- **Botones (18):** T.O CONFIG, ENG, BLEED, PRESS, ELEC, HYD, FUEL, APU, COND, DOOR, WHEEL, FCTL, ALL, CLR(1), STS, RCL, CLR(2), EMER CANC
- **Pines utilizados:** 18/20

### UNO 4 - PEDESTAL (PUMS)
- **Botones (6):** PUMS 1, PUMS 2, PUMS 3, PUMS 4, PUMS 5, PUMS 6
- **Pines utilizados:** 6/20

### MEGA 4 - MCDU
- **Botones (70):** LSK(12), PAGE(12), SLEW(4), A NUM(42)
- **Pines utilizados:** 70/70 (justo)

## CONEXIÓN USB
Cada placa se conecta a un **Hub USB 10 puertos con alimentación**.
- Total puertos requeridos: 8 (4 Megas + 4 Unos)
- Se recomienda hub con fuente 5V/12V para alimentación estable.

## ACTUALIZACIONES
Esta distribución puede ajustarse según disponibilidad de componentes.
Última revisión: $(date +%Y-%m-%d)
