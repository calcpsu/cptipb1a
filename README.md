# CalcPack TI BP1A

A Li-Po battery replacement design for TI BP1A battery pack calculators - primarily TI-59. The original batteries had ~ 500mAh capacity (@3.6V: 1.8Wh), while modern Ni-MH replacements are typically ~1500mAh (@3.6V: 5.4Wh).

Li-Po has the advantage of far reduced self-discharge in comparison to Ni-MH, which is an advantage for an intermittently-used device. Even with similar mAh capacity, we can expect longer battery life.

Ni-MH / Ni-CD batteries are notorious for leaking. While Lithium Ion batteries are notorious for self-immolation, a well protected Li-Po battery (particularly in a low current application like this) should be able to be made very safe.

![Render of calcpack PCB](https://github.com/calcpsu/cptipb1a/blob/main/render.png?raw=true)

## Features / design goals:
- Direct replacement for a BP1A battery pack
- Compatible with existing charging circuit (although at a slow charge rate)
    - Provides adequate smoothing of rectified AC
    - Provides voltage clamping
- USB charging (when removed from calculator) at faster rate
- Protected from:
    - Overvoltage (USB and pads) at 2x rated voltage and current (IATA requirement)
    - Overcharging (4.2V)
    - Over-discharge (3.1V shutdown, 2.5V cutoff in battery pack)
    - Short circuit and overcurrent (again for IATA requirement)
- Minimum idle/quiescent current to maximise charge time
- Capable of operating TI-59 including card reader
- Similar or higher capacity than typical Ni-MH altenative (1500mAh @ 3.7V [5.55Wh])
  
## License

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
