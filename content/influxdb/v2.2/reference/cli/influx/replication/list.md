---
title: influx replication list
description: List InfluxDB replication streams and corresponding metrics.
menu:
  influxdb_2_1_ref:
    name: influx replication list
    parent: influx replication
weight: 102
influxdb/v2.1/tags: [write, replication]
related:
  - /influxdb/v2.1/reference/cli/influx/replication
---

The `influx replication list` command lists all InfluxDB replication streams and their corresponding metrics.

## Usage
```
influx replication list [command options] [arguments...]
```

## Flags
| Flag |                   | Description                                                           | Input type | {{< cli/mapped >}}    |
| :--- | :---------------- | :-------------------------------------------------------------------- | :--------: | :-------------------- |
| `-n` | `--name`          | Filter replication streams by name                                    |   string   |                       |
|      | `--org-id`        | Local organization ID                                                 |   string   | `INFLUX_ORG_ID`       |
| `-o` | `--org`           | Local organization name                                               |   string   | `INFLUX_ORG`          |
|      | `--remote-id`     | Filter replication streams by remote connection ID                    |   string   |                       |
|      | `--local-bucket`  | Filter replication streams by local bucket                            |   string   |                       |
|      | `--host`          | InfluxDB HTTP address (default `http://localhost:8086`)               |   string   | `INFLUX_HOST`         |
|      | `--skip-verify`   | Skip TLS certificate verification                                     |            | `INFLUX_SKIP_VERIFY`  |
|      | `--configs-path`  | Path to `influx` CLI configurations (default `~/.influxdbv2/configs`) |   string   | `INFLUX_CONFIGS_PATH` |
| `-c` | `--active-config` | CLI configuration to use for command                                  |   string   |                       |
|      | `--http-debug`    | Inspect communication with InfluxDB servers                           |   string   |                       |
|      | `--json`          | Output data as JSON (default `false`)                                 |            | `INFLUX_OUTPUT_JSON`  |
|      | `--hide-headers`  | Hide table headers (default `false`)                                  |            | `INFLUX_HIDE_HEADERS` |
| `-t` | `--token`         | InfluxDB API token                                                    |   string   | `INFLUX_TOKEN`        |