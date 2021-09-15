# Nibe to influxdb via telegraf.

Docker instance to query a NIBE S1255 machine and send operational values with
telegraf to a influxdb. The values can be found from the NIBE s-series manual
and depend on the installation. Current values try to fit a default
installation. Any failures will show an annoying modbus -1 exception that's hard
to debug. Just remove values until you find the correct offending one.

## Setup

Create a .env file with your environments config, e.g.

```
NIBE_HOST=10.0.0.10
INFLUXDB_HOST="influxdb.com:8086"
INFLUXDB_DB=db0
INFLUXDB_USER=user
INFLUXDB_PASS=password
```

## Run

```
docker-compose build
docker-compose up
```
