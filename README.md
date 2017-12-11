# The US pipelines incidents
### From 2010 to October 2017

A Jupyter notebook to analyze trends in pipeline incidents in the US from 2010
to October 2017. Different aspects of the incidents are considered to answer these
five questions:

1. How common are spills?
2. What is their spatial and temporal distributions?
2. What is their scale regarding volume and cost?
2. What are the main causes of spills?
3. What places have a higher risk?

![map](/incident_ditribution.png)
![states](/incident_states.png)

# How it works?
At this moment, all the code is in `pipeline.ipynb` file. It mainly performs the
following actions:
* Checks the latest update in the dataset. If the date is more than `number_of_days` variable,
it downloads the latest dataset from the server and replaces the old dataset locally.
* Extracts the required columns from the dataset, cleans the values (both text and `NaN`) and converts
the units to more useful ones. Finally it saves the cleaned dataset locally. It also
exports a `json` file containing the summary of data. This file will be used to create a
website which shows the summary using D3 library.
* Plots multiple figures showing temporal and spatial trends in spills and their
financial and environmental damage.
* Some figures are exported to be used in the [README](README.md) file and the final report.

## Required libraries
* numpy
* pandas
* matplotlib
* plotly

## Dataset
The dataset contains 'Flagged Incidents' from PHMSA Pipeline Safety [website](https://www.phmsa.dot.gov/data-and-statistics/pipeline/pipeline-incident-flagged-files).

## Authors
Mahdi Sadjadi - http://mahdisadjadi.com/

## Reference
This repository is also published as a
[blog post](http://mahdisadjadi.com/blog/20161203_pipeline/).

## License
This project is licensed under the MIT License - see the LICENSE.md file
for details. The dataset is downloaded from [PHMSA](http://www.phmsa.dot.gov/).
