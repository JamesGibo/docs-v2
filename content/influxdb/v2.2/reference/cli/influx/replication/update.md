---
title: influx replication update
description: Update InfluxDB replication streams.
menu:
  influxdb_2_1_ref:
    name: influx replication update
    parent: influx replication
weight: 102
influxdb/v2.1/tags: [write, replication]
related:
  - /influxdb/v2.1/reference/cli/influx/replication
---

The `influx replication update` command updates an InfluxDB replication stream.

## Usage
```
influx replication update [command options] [arguments...]
```

## Flag 
  
| Flag |                                | Description                                                           | Input type | {{< cli/mapped >}}    |
| :--- | :----------------------------- | :-------------------------------------------------------------------- | :--------: | :-------------------- |
| `-i` | `--id`                         | Replication stream ID to update                                       |   string   |                       |
| `-n` | `--name`                       | New replication stream name                                           |   string   |                       |
| `-d` | `--description`                | New replication stream description                                    |   string   |                       |
|      | `--remote-id`                  | New remote connection ID to send data to                              |   string   |                       |
|      | `--remote-bucket`              | New remote bucket ID to replicate data to                             |   string   |                       |
|      | `--max-queue-bytes`            | New max queue size in bytes (default: `0`)                            |  integer   |                       |
|      | `--drop-non-retryable-data`    | Drop data when a non-retryable error is encountered                   |            |                       |
|      | `--no-drop-non-retryable-data` | Do not drop data when a non-retryable error is encountered            |            |                       |
|      | `--host`                       | InfluxDB HTTP address (default `http://localhost:8086`)               |   string   | `INFLUX_HOST`         |
|      | `--skip-verify`                | Skip TLS certificate verification                                     |            | `INFLUX_SKIP_VERIFY`  |
|      | `--configs-path`               | Path to `influx` CLI configurations (default `~/.influxdbv2/configs`) |   string   | `INFLUX_CONFIGS_PATH` |
| `-c` | `--active-config`              | CLI configuration to use for command                                  |   string   |                       |
|      | `--http-debug`                 | Inspect communication with InfluxDB servers                           |   string   |                       |
|      | `--json`                       | Output data as JSON (default `false`)                                 |            | `INFLUX_OUTPUT_JSON`  |
|      | `--hide-headers`               | Hide table headers (default `false`)                                  |            | `INFLUX_HIDE_HEADERS` |
| `-t` | `--token`                      | InfluxDB API token                                                    |   string   | `INFLUX_TOKEN`        |