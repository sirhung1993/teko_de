# Teko Data Engineer

## System Requirements

- Docker version >= 18.09.6
- docker-compose version >= 1.23.2
- Linux 4.15.0-50-generic(tested)

## Demo processes

1. Download sample data at [New York City Taxi](https://www.kaggle.com/kentonnlp/2014-new-york-city-taxi-trips).
2. Clone git repository and change current dicrectory to project folder ```cd <path/to/project>```
3. Put the downloaded csv in ***sample-data/*** with name ***nyc_taxi_data_2014.csv***
4. Load data from csv by running this command: ```docker-compose -f load_data.yml up``` to Elasticsearch
5. Wait several minutes to load few sample data (due to demo purposes, no need to load full 15 mil rows of data).
6. Exit the process by pressing ```Ctrl + C``` or ```docker container kill <container_id>```
7. Start Elasticsearch and Kibana by running ```docker-compose up```
8. Open browser and visit: ***localhost:5601***
9. If Kibana does not load the default setting, import json setting file by using : ***kibana-setting/nyc-taxi.json***
10. Enjoy my free-style data visuallize!

## Notes

- Due to the runtime environment differences, there may be some configurations issues relating to docker or docker-compose
  