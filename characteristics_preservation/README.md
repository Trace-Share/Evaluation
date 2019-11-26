# Evaluation of Statistical Characteristics Preservation

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3547528.svg)](https://doi.org/10.5281/zenodo.3547528)

The directory contains a summary of results for the evaluation of statistical characteristics preservation. Raw data with all traces, together with computed statistics, are available at [https://doi.org/10.5281/zenodo.3547528](https://doi.org/10.5281/zenodo.3547528).


## Selected Attack Traces

We selected 72 different traces of network attacks obtained from various internet databases. File names refer to common names of contained vulnerabilities, malware, or attack tools.


## Background Traffic Data

Publicly available dataset [CSE-CIC-IDS-2018](https://www.unb.ca/cic/datasets/ids-2018.html) was used as a background traffic data. The evaluation uses data from the day Thursday-01-03-2018 containing a sufficient proportion of regular traffic without any statistically significant attacks. Only traffic aimed at victim machines (range 172.31.69.0/24) is used to reduce less significant traffic.


## Dataset Structure

* Traces variants ([traces-normalized.zip](https://zenodo.org/record/3547528/files/traces.zip), [traces-adjusted.zip](https://zenodo.org/record/3547528/files/traces.zip) -- password: "*trace-share*")
    * `./traces-normalized/` -- normalized PCAP files and details in YAML format;
    * `./traces-adjusted/` -- configuration files for traces combination in YAML format.
* Computed statistics ([statistics.zip](https://zenodo.org/record/3547528/files/alerts.zip) -- password: "*trace-share*")
    * `./statistics-background/` -- background traffic statistics computed by ID2T;
    * `./statistics-combination/` -- combined traces statistics computed by ID2T for all adjust options (selected only combinations where ID2T provided all statistics files);
    * `./statistics-difference/` -- computed mean and median differences of background and combined traffic traces.
* Evaluation results 
    * `statistics-difference.ipynb` -- file containing visualization of statistics differences.


## Cooperation

*If you are interested in research collaborations, don't hesitate to contact us at  [https://csirt.muni.cz](https://csirt.muni.cz/about-us/contact?lang=en)!*
