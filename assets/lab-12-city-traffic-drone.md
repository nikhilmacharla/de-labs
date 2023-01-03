# City Traffic Drone

## Objective

City Vehicle Trajactories Data extraction and warehousing for Traffic analysis

A city traffic department wants to collect traffic data using swarm UAVs (drones) from a number of locations in the city and use the data collected for improving traffic flow in the city and for a number of other undisclosed projects. Your startup is responsible for creating a scalable data warehouse that will host the vehicle trajectory data extracted by analysing footage taken by swarm drones and static roadside cameras. The data warehouse should take into account future needs, organise data such that a number of downstream projects query the data efficiently. You should use the Extract Load Transform (ELT) framework using DBT.

![](https://user-images.githubusercontent.com/62965911/210303733-e7ea713c-1fe0-47cb-ad60-842ec5d19c19.png)

Process steps:

1. Download the data from https://open-traffic.epfl.ch/index.php/downloads (optional)
2. Configure the project paths in the DAG
3. Run the DAG

## Dashboard

![](https://user-images.githubusercontent.com/62965911/210303740-f6e3b6ff-c78c-478d-bb7c-d8fbdd6e81e6.png)

## Solution

```
.
├── [ 23K]  01-sa-main.ipynb
├── [ 148]  data
│   └── [  52]  download.sh
├── [1.0M]  dbt_
│   ├── [ 314]  dbt_project.yml
│   ├── [227K]  logs
│   │   └── [227K]  dbt.log
│   ├── [4.6K]  models
│   │   ├── [ 225]  dim_types.sql
│   │   ├── [ 120]  distance_distribution.sql
│   │   ├── [ 356]  fast_vehicles.sql
│   │   ├── [ 209]  fast_vehicles_summary.sql
│   │   ├── [ 471]  fct_summary.sql
│   │   ├── [ 454]  fct_trajectory.sql
│   │   ├── [ 153]  lat_timely_summary.sql
│   │   ├── [ 154]  lon_timely_summary.sql
│   │   ├── [ 115]  max_distance.sql
│   │   ├── [ 110]  max_speed.sql
│   │   ├── [ 109]  max_time.sql
│   │   ├── [ 242]  schema.yml
│   │   ├── [ 110]  speed_distribution.sql
│   │   ├── [ 151]  speed_timely_summary.sql
│   │   ├── [ 108]  time_distribution.sql
│   │   ├── [ 400]  timely_summary.sql
│   │   ├── [ 108]  type_distribution.sql
│   │   └── [ 460]  vehicles_summary.sql
│   ├── [ 266]  profiles.yml
│   ├── [ 73K]  seeds
│   │   ├── [ 11K]  endpoints_location.csv
│   │   └── [ 61K]  endpoints_trafficinfo.csv
│   ├── [759K]  target
│   │   ├── [4.4K]  compiled
│   │   │   └── [4.3K]  VehicleTrajectory
│   │   │       └── [4.2K]  models
│   │   │           ├── [ 201]  dim_types.sql
│   │   │           ├── [ 128]  distance_distribution.sql
│   │   │           ├── [ 332]  fast_vehicles.sql
│   │   │           ├── [ 200]  fast_vehicles_summary.sql
│   │   │           ├── [ 470]  fct_summary.sql
│   │   │           ├── [ 453]  fct_trajectory.sql
│   │   │           ├── [ 144]  lat_timely_summary.sql
│   │   │           ├── [ 144]  lon_timely_summary.sql
│   │   │           ├── [ 123]  max_distance.sql
│   │   │           ├── [ 118]  max_speed.sql
│   │   │           ├── [ 117]  max_time.sql
│   │   │           ├── [ 118]  speed_distribution.sql
│   │   │           ├── [ 142]  speed_timely_summary.sql
│   │   │           ├── [ 116]  time_distribution.sql
│   │   │           ├── [ 377]  timely_summary.sql
│   │   │           ├── [ 116]  type_distribution.sql
│   │   │           └── [ 437]  vehicles_summary.sql
│   │   ├── [ 22K]  graph.gpickle
│   │   ├── [348K]  manifest.json
│   │   ├── [339K]  partial_parse.msgpack
│   │   ├── [ 36K]  run
│   │   │   └── [ 36K]  VehicleTrajectory
│   │   │       ├── [5.8K]  models
│   │   │       │   ├── [ 299]  dim_types.sql
│   │   │       │   ├── [ 222]  distance_distribution.sql
│   │   │       │   ├── [ 418]  fast_vehicles.sql
│   │   │       │   ├── [ 294]  fast_vehicles_summary.sql
│   │   │       │   ├── [ 570]  fct_summary.sql
│   │   │       │   ├── [ 556]  fct_trajectory.sql
│   │   │       │   ├── [ 235]  lat_timely_summary.sql
│   │   │       │   ├── [ 235]  lon_timely_summary.sql
│   │   │       │   ├── [ 208]  max_distance.sql
│   │   │       │   ├── [ 200]  max_speed.sql
│   │   │       │   ├── [ 198]  max_time.sql
│   │   │       │   ├── [ 209]  speed_distribution.sql
│   │   │       │   ├── [ 235]  speed_timely_summary.sql
│   │   │       │   ├── [ 206]  time_distribution.sql
│   │   │       │   ├── [ 464]  timely_summary.sql
│   │   │       │   ├── [ 206]  type_distribution.sql
│   │   │       │   └── [ 526]  vehicles_summary.sql
│   │   │       └── [ 30K]  seeds
│   │   │           ├── [ 976]  endpoints_location.csv
│   │   │           └── [ 29K]  endpoints_trafficinfo.csv
│   │   └── [9.4K]  run_results.json
│   └── [ 888]  tests
│       ├── [ 385]  test_distributions.sql
│       └── [ 375]  test_summaries.sql
├── [1.0M]  img
│   ├── [278K]  front.png
│   └── [753K]  redash.png
└── [1.1K]  lab-12-city-traffic-drone.md

 2.1M used in 15 directories, 70 files
```