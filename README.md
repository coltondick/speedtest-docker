# speedtest-docker

Docker Container to run a speedtest and send the metrics to influxdb.

## Installation

1. Clone the repository:

```shell
git clone https://github.com/coltondick/speedtest-docker
```

3. Create a copy of the sample `.env` file and edit the .env file accordingly:

```shell
cp .env.sample .env
```

4. Start the container:

```shell
docker-compose up -d
```

## Configuration

You can make use of the following environment variables / configurations:

| Environment variable | Default value | Description                                                                |
| -------------------- | ------------- | -------------------------------------------------------------------------- |
| `SPEEDTEST_INTERVAL` | `300`         | Interval/pause (in seconds) between speedtests                             |
| `SPEEDTEST_HOST`     | `local`       | Display name of the client                                                 |
| `SPEEDTEST_SERVER`   | none          | Optionally set specific speedtest.net server ID, otherwise use the closest |
| `INFLUXDB_DB`        | `speedtest`   | Database to save speedtest results                                         |
| `INFLUXDB_HOST`      | `influxdb`    | Name of the InfluxDB host/containers                                       |
| `INFLUXDB_USERNAME`  | `root`        | Username for InfluxDB authentication                                       |
| `INFLUXDB_PASSWORD`  | `root`        | Password for InfluxDB authentication                                       |
