# Overview of the events.csv files across the LéXPLORE datasets

## Standard

The suggested structure of the `events.csv` file mainly follows the structure of the temperature chain

| start             | stop              | parameter | depth                              | comments              |
| ----------------- | ----------------- | --------- | ---------------------------------- | --------------------- |
| 20190617 00:00:00 | 20190620 14:00:00 | All       | All                                | Initial deployment    |
| 20190822 10:00:00 | 20191025 00:00:00 | All       | All                                | Cable broken. No data |
| 20191025 00:00:00 | 20200418 00:00:00 | All       | 2.5,4,7,10,12,13,15,18,21,27,48,51 | Sensor failure        |

## Current state

### [Meteorological station](https://github.com/LeXPLORE-Platform/Meteostation/)

The [`events.csv`](https://github.com/LeXPLORE-Platform/Meteostation/blob/master/notes/events.csv) file is located in the `notes` folder. It contains 2 entries, in the format

| start             | stop              | parameter | Comments      |
| ----------------- | ----------------- | --------- | ------------- |
| 20220510 00:00:00 | 20221026 12:30:00 | Rain      | sensor broken |
| 20221024 12:00:00 | 20221024 12:30:00 | All       | Maintenance   |

As of the 22.01.2026, the file is never used in the processing described in [`main.py`](https://github.com/LeXPLORE-Platform/Meteostation/blob/master/scripts/main.py).

### [Wave buoy](https://github.com/LeXPLORE-Platform/wave-buoy)

The [`events.csv`](https://github.com/LeXPLORE-Platform/wave-buoy/blob/master/notes/events.csv) file is located in the `notes` folder. It contains 1 entry, in the format

| Start date | Start time | Stop date | Stop time | parameter | Comments           | Operator           |
| ---------- | ---------- | --------- | --------- | --------- | ------------------ | ------------------ |
| 20021019   | 13:20:00   | 20221026  | 13:40:00  | all       | Bad com, extrafile | Sebastien Lavanchy |

As of the 22.01.2026, the file is never used in the processing described in [`main.py`](https://github.com/LeXPLORE-Platform/wave-buoy/blob/master/scripts/main.py).

### ADCP velocities - [Deep and near-surface](https://github.com/LeXPLORE-Platform/acousticdopplercurrentprofiler)

The [`events.csv`](https://github.com/LeXPLORE-Platform/acousticdopplercurrentprofiler/blob/master/notes/events.csv) file is located in the `notes` folder. It contains 1 entry, in the format

| Start date | Start time | Stop date | Stop time | parameter | Comments    |
| ---------- | ---------- | --------- | --------- | --------- | ----------- |
| 20210625   | 07:29:00   | 20220625  | 17:33:00  | all       | Maintenance |

As of the 22.01.2026, the file is never used in the processing described in [`main.py`](https://github.com/LeXPLORE-Platform/acousticdopplercurrentprofiler/blob/master/scripts/main.py).

### [Temperature chain](https://github.com/LeXPLORE-Platform/thermister-chain)

The [`events.csv`](https://github.com/LeXPLORE-Platform/thermister-chain/blob/master/notes/events.csv) file is located in the `notes` folder. It contains 76 entries, in the format

| start             | stop              | parameter | depth                              | comments              |
| ----------------- | ----------------- | --------- | ---------------------------------- | --------------------- |
| 20190617 00:00:00 | 20190620 14:00:00 | All       | All                                | Initial deployment    |
| 20190822 10:00:00 | 20191025 00:00:00 | All       | All                                | Cable broken. No data |
| 20191025 00:00:00 | 20200418 00:00:00 | All       | 2.5,4,7,10,12,13,15,18,21,27,48,51 | Sensor failure        |
| ...               | ...               | ...       | ...                                |                       |

The file is used in [`main.py`](https://github.com/LeXPLORE-Platform/thermister-chain/blob/master/scripts/main.py).

### [Idronaut](https://github.com/LeXPLORE-Platform/idronaut-automatic-profiler)

The [`events.csv`](https://github.com/LeXPLORE-Platform/idronaut-automatic-profiler/blob/master/notes/events.csv) file is located in the `notes` folder. It contains 0 entries, in the format

| start | stop | parameter | Comments |
| ----- | ---- | --------- | -------- |

As of the 22.01.2026, the file is never used in the processing described in [`main.py`](https://github.com/LeXPLORE-Platform/idronaut-automatic-profiler/blob/master/scripts/main.py)

### [Thetis - physico-chemical, optical](https://github.com/LeXPLORE-Platform/thetis-multi-instrument-profiler)

As of 22.01.2026, no `events.csv` in the [Thetis Multi Instrument Profiler](https://github.com/LeXPLORE-Platform/thetis-multi-instrument-profiler) repository

### [Sea and Sun CTD](https://github.com/LeXPLORE-Platform/platform-ctd-profiles)

As of 22.01.2026, no `events.csv` in the [Platform CTD Profiles](https://github.com/LeXPLORE-Platform/platform-ctd-profiles) repository

### [OxyPAR mooring](https://github.com/LeXPLORE-Platform/ppmooring)

As of 22.01.2026, no `events.csv` in the [OxyPAR mooring](https://github.com/LeXPLORE-Platform/ppmooring) repository.
