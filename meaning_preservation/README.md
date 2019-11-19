# Evaluation of Trace Meaning Preservation

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3547528.svg)](https://doi.org/10.5281/zenodo.3547528)

The file contains a summary of results for the evaluation of trace meaning preservation. Raw data with all traces and their variants, together with Suricata analysis results, are available at [https://doi.org/10.5281/zenodo.3547528](https://doi.org/10.5281/zenodo.3547528).


## Selected Attack Traces

The following list contains trace datasets used for evaluation. Each attack was chosen to have not only a different meaning but also different statistical properties.

* **dos_http_flood** -- the capture of GET and POST requests sent to one server by one attacker (HTTP~traffic);
* **ftp_bruteforce** -- short and unsuccessful attempt to guess a user’s password for FTP service (FTP traffic);
* **ponyloader_botnet** -- Pony Loader botnet used for stealing of credentials from 3 target devices reporting to single IP with a large number of intermediate addresses (DNS and HTTP traffic);
* **scan** -- the capture of nmap tool that scans given subnet using ICMP echo and TCP SYN requests (consist of ARP, ICMP, and TCP traffic);
* **wannacry_ransomware** -- the capture of Wanacry ransomware that spreads in a domain with three workstations, a domain controller, and a file-sharing server (SMB and SMBv2 traffic).


## Background Traffic Data

Publicly available dataset [CSE-CIC-IDS-2018](https://www.unb.ca/cic/datasets/ids-2018.html) was used as a background traffic data. The evaluation uses data from the day Thursday-01-03-2018 containing a sufficient proportion of regular traffic without any statistically significant attacks. Only traffic aimed at victim machines (range 172.31.69.0/24) is used to reduce less significant traffic.


## Dataset Structure

* Traces variants ([traces.zip](https://zenodo.org/record/3547528/files/traces.zip) -- password: "*trace-share*")
    * `./traces-original/` -- trace PCAP files and crawled details in YAML format;
    * `./traces-normalized/` -- normalized PCAP files and details in YAML format;
    * `./traces-adjusted/` -- adjusted PCAP files using various timestamp generation settings, combination configuration in YAML format, and lables provided by ID2T in XML format.
* Extracted alerts ([alerts.zip](https://zenodo.org/record/3547528/files/alerts.zip) -- password: "*trace-share*")
    * `./alerts-original/` -- extracted Suricata alerts, Suricata log, and full Suricata output for all original trace files;
    * `./alerts-normalized/` -- extracted Suricata alerts, Suricata log, and full Suricata output for all normalized trace files;
    * `./alerts-adjusted/` -- extracted Suricata alerts, Suricata log, and full Suricata output for all adjusted trace files.
* Evaluation results 
    * `.csv` files in the root directory -- data contains extracted alert signatures and their count per each trace variant.


## Cooperation

*If you are interested in research collaborations, don't hesitate to contact us at  [https://csirt.muni.cz](https://csirt.muni.cz/about-us/contact?lang=en)!*
