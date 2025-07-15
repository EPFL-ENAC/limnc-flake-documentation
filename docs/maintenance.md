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

| start | stop | parameter | Comments |
| ----- | ---- | --------- | -------- |

### [Wave buoy](https://gitlab.renkulab.io/lexplore/wave-buoy)

The [`events.csv`](https://gitlab.renkulab.io/lexplore/wave-buoy/-/blob/master/notes/events.csv?ref_type=heads) file is located in the `notes` folder. It contains 1 entry, in the format

| Start date | Start time | Stop date | Stop time | parameter | Comments | Operator |
| ---------- | ---------- | --------- | --------- | --------- | -------- | -------- |

### [ADCP velocities](https://gitlab.renkulab.io/lexplore/adcp)

No `events.csv` in the [ADCP 19-20](https://gitlab.renkulab.io/lexplore/adcp) repository

### [Temperature chain](https://gitlab.renkulab.io/lexplore/thermister-chain)

The [`events.csv`](https://gitlab.renkulab.io/lexplore/thermister-chain/-/blob/master/notes/events.csv?ref_type=heads) file is located in the `notes` folder. It contains 2 entries, in the format

| start             | stop              | parameter | depth                              | comments              |
| ----------------- | ----------------- | --------- | ---------------------------------- | --------------------- |
| 20190617 00:00:00 | 20190620 14:00:00 | All       | All                                | Initial deployment    |
| 20190822 10:00:00 | 20191025 00:00:00 | All       | All                                | Cable broken. No data |
| 20191025 00:00:00 | 20200418 00:00:00 | All       | 2.5,4,7,10,12,13,15,18,21,27,48,51 | Sensor failure        |

### [Idronaut](https://gitlab.renkulab.io/lexplore/idronaut-automatic-profiler)

The [`events.csv`](https://gitlab.renkulab.io/lexplore/idronaut-automatic-profiler/-/blob/master/notes/events.csv?ref_type=heads) file is located in the `notes` folder. It contains 0 entries, in the format

| start | stop | parameter | Comments |
| ----- | ---- | --------- | -------- |

### [Thetis - physico-chemical, optical](https://gitlab.renkulab.io/lexplore/thetis-multi-instrument-profiler)

No `events.csv` in the [ADCP 19-20](https://gitlab.renkulab.io/lexplore/thetis-multi-instrument-profiler) repository

### [Sea and Sun CTD](https://gitlab.renkulab.io/lexplore/platform-ctd-profiles)

No `events.csv` in the [ADCP 19-20](https://gitlab.renkulab.io/lexplore/platform-ctd-profiles) repository

### OxyPAR mooring
