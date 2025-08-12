# Quality assurance (QA) JSON

Each repository outlined in [datasets][datasets] contains a JSON file allowing the data curator to define the QA/QC processes for that dataset. This JSON file will subsequently be used as input by the [envass][envass] Python package.

The envass packages to identify

- values that are not considered numerical
- values which are not in the range specified by the bounds
- values on the edges of the data set
- values which are not (strictly) increasing/decreasing
- values outside the interquartile range (IQR) for timeseries data
- values exceeding a defined variation rate threshold
- outlier values based on an IQR for a window of time series data
- outlier values based on kmean clustering
- outlier values based on kmean clustering and threshold value

## Example

An example of a QA JSON can be found in idronaut-automatic-profiler repository:

```JSON
{
  "time": {"simple": {"numeric": "True", "bounds": [1514764800, "now"]}, "advanced": {}},
  "Press": {"simple": {"numeric": "True", "bounds": [0, 310]}, "advanced": {}},
  "Temp": {"simple": {"numeric": "True", "bounds": [-5, 40]}, "advanced": {}},
  "Cond": {"simple": {"numeric": "True", "bounds": [0, 100]}, "advanced": {}},
  "Sal": {"simple": {"numeric": "True", "bounds": [0, 5]}, "advanced": {}},
  "O2pc": {"simple": {"numeric": "True", "bounds": [0, 150]}, "advanced": {}},
  "O2ppm": {"simple": {"numeric": "True", "bounds": [0,14]}, "advanced": {}},
  "pH": {"simple": {"numeric": "True", "bounds": [0,14]}, "advanced":{}},
  "eH": {"simple": {"numeric": "True", "bounds": [0,10000]}, "advanced": {}},
  "PAR": {"simple": {"numeric": "True", "bounds": [-500,500]}, "advanced": {}},
  "O2pc_2": {"simple": {"numeric": "True", "bounds": [0,150]}, "advanced": {}},
  "O2ppm_2": {"simple": {"numeric": "True", "bounds": [0,14]}, "advanced": {}},
  "Chl": {"simple": {"numeric": "True", "bounds": [0,50]}, "advanced": {}},
  "PhycoEr": {"simple": {"numeric": "True", "bounds": [-50,50]}, "advanced": {}},
  "PhycoCy": {"simple": {"numeric": "True", "bounds": [-50,50]}, "advanced": {}}
}
```

For each variable outlined in the JSON, the automated QA/QC process will identify values that are not numerical (via the `"numeric": "True"`) and/or outside of specific bounds (e.g, `"bounds": [-5, 40]` for the temperature).

[datasets]: datasets.md
[envass]: https://pypi.org/project/envass/
