# Original network models 
https://github.com/deakinmt/uk-mvlv-models

# vehicle-grid-integration-opendss-networks
Vehicle Grid Integration OpenDSS Networks

* This repo stores the networks that the OpenDSS web back-end uses
* A GitHub Action uploads networks in `vgiwebprodopendssnetworks`
* The destination is our Azure Storage Container `vgiwebprodopendssnetworks`
* It will upload on a push to `main`
* The BlobEndpoint is held in a repo secret `NETWORKS_DATA_CONTAINER_CONNECTION_STRING`
* That SAS token will expire 2022-12-31

## zip file structure should match
* forward slash path separators
* LF line endings

```
├── buscoords.csv
├── generators.dss
├── lds_edit.dss
├── lines.dss
├── loads.dss
├── lvNetworks
│   ├── network_11_1_1144
│   │   ├── Feeder_1
│   │   │   ├── LineCode.txt
│   │   │   ├── LinesUnq_pruned.txt
│   │   │   ├── LinesUnq_pruned1_1144.txt
│   │   │   ├── LoadsCopyUnq.txt
│   │   │   ├── LoadsCopyUnq1_1144.txt
│   │   │   ├── Transformers.txt
│   │   │   ├── Transformers_mod.txt
│   │   │   ├── Transformers_mod1_1144.txt
│   │   │   ├── Transformers_one_mod.txt
│   │   │   └── XY_Position1_1144.csv
...
├── master_mvlv.dss
├── redirect_lv_ntwx.dss
├── regcontrols.dss
└── transformers.dss
```
