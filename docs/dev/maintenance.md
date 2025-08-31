# Overview of the events.csv files across the LéXPLORE datasets

## Standard

The suggested structure of the `events.csv` file mainly follows the structure of the temperature chain

| start             | stop              | parameter | depth                              | comments              |
| ----------------- | ----------------- | --------- | ---------------------------------- | --------------------- |
| 20190617 00:00:00 | 20190620 14:00:00 | All       | All                                | Initial deployment    |
| 20190822 10:00:00 | 20191025 00:00:00 | All       | All                                | Cable broken. No data |
| 20191025 00:00:00 | 20200418 00:00:00 | All       | 2.5,4,7,10,12,13,15,18,21,27,48,51 | Sensor failure        |

## Current state

### [Meteorological station](https://gitlab.renkulab.io/lexplore/meteostation)

The [`events.csv`](https://gitlab.renkulab.io/lexplore/meteostation/-/blob/master/notes/events.csv?ref_type=heads) file is located in the `notes` folder. It contains 2 entries, in the format

| start             | stop              | parameter | Comments      |
| ----------------- | ----------------- | --------- | ------------- |
| 20220510 00:00:00 | 20221026 12:30:00 | Rain      | sensor broken |
| 20221024 12:00:00 | 20221024 12:30:00 | All       | Maintenance   |

The file is never used in the processing described in [`main.py`](https://gitlab.renkulab.io/lexplore/meteostation/-/blob/master/scripts/main.py).

### [Wave buoy](https://gitlab.renkulab.io/lexplore/wave-buoy)

The [`events.csv`](https://gitlab.renkulab.io/lexplore/wave-buoy/-/blob/master/notes/events.csv?ref_type=heads) file is located in the `notes` folder. It contains 1 entry, in the format

| Start date | Start time | Stop date | Stop time | parameter | Comments           | Operator           |
| ---------- | ---------- | --------- | --------- | --------- | ------------------ | ------------------ |
| 20021019   | 13:20:00   | 20221026  | 13:40:00  | all       | Bad com, extrafile | Sebastien Lavanchy |

The file is never used in the processing described in [`main.py`](https://gitlab.renkulab.io/lexplore/wave-buoy/-/blob/master/scripts/main.py).

### ADCP velocities - [Deep](https://gitlab.renkulab.io/lexplore/acousticdopplercurrentprofiler) & [Surface](https://gitlab.renkulab.io/lexplore/adcp)

No `events.csv` in the [Acoustic Doppler Current Profiler](https://gitlab.renkulab.io/lexplore/acousticdopplercurrentprofiler) repository

### [Temperature chain](https://gitlab.renkulab.io/lexplore/thermister-chain)

The [`events.csv`](https://gitlab.renkulab.io/lexplore/thermister-chain/-/blob/master/notes/events.csv?ref_type=heads) file is located in the `notes` folder. It contains 76 entries, in the format

| start             | stop              | parameter | depth                              | comments              |
| ----------------- | ----------------- | --------- | ---------------------------------- | --------------------- |
| 20190617 00:00:00 | 20190620 14:00:00 | All       | All                                | Initial deployment    |
| 20190822 10:00:00 | 20191025 00:00:00 | All       | All                                | Cable broken. No data |
| 20191025 00:00:00 | 20200418 00:00:00 | All       | 2.5,4,7,10,12,13,15,18,21,27,48,51 | Sensor failure        |
| ...               | ...               | ...       | ...                                |                       |

The file is used in [`main.py`](https://gitlab.renkulab.io/lexplore/thermister-chain/-/blob/master/scripts/main.py).

### [Idronaut](https://gitlab.renkulab.io/lexplore/idronaut-automatic-profiler)

The [`events.csv`](https://gitlab.renkulab.io/lexplore/idronaut-automatic-profiler/-/blob/master/notes/events.csv?ref_type=heads) file is located in the `notes` folder. It contains 0 entries, in the format

| start | stop | parameter | Comments |
| ----- | ---- | --------- | -------- |

The file is never used in the processing described in [`main.py`](https://gitlab.renkulab.io/lexplore/idronaut-automatic-profiler/-/blob/master/scripts/main.py).

### [Thetis - physico-chemical, optical](https://gitlab.renkulab.io/lexplore/thetis-multi-instrument-profiler)

No `events.csv` in the [Thetis Multi Instrument Profiler](https://gitlab.renkulab.io/lexplore/thetis-multi-instrument-profiler) repository

### [Sea and Sun CTD](https://gitlab.renkulab.io/lexplore/platform-ctd-profiles)

No `events.csv` in the [Platform CTD Profiles](https://gitlab.renkulab.io/lexplore/platform-ctd-profiles) repository

### [OxyPAR mooring](https://gitlab.renkulab.io/lexplore/ppmooring)

No `events.csv` in the [OxyPAR mooring](https://gitlab.renkulab.io/lexplore/ppmooring) repository.
