---
title: date.monthDay() function
description: >
  The `date.monthDay()` function returns the day of the month for a specified time.
  Results range from `[1-31]`.
aliases:
  - /influxdb/v2.0/reference/flux/functions/date/monthday/
  - /influxdb/v2.0/reference/flux/stdlib/date/monthday/
  - /influxdb/cloud/reference/flux/stdlib/date/monthday/
menu:
  flux_0_x_ref:
    name: date.monthDay
    parent: date
weight: 301
introduced: 0.37.0
---

The `date.monthDay()` function returns the day of the month for a specified time.
Results range from `[1-31]`.

```js
import "date"

date.monthDay(t: 2019-07-17T12:05:21.012Z)

// Returns 17
```

## Parameters

### t {data-type="time, duration"}
The time to operate on.
Use an absolute time, relative duration, or integer.
Durations are relative to `now()`.

## Examples

##### Return the day of the month for a time value
```js
import "date"

date.monthDay(t: 2020-02-11T12:21:03.293534940Z)

// Returns 11
```

##### Return the day of the month for a relative duration
```js
import "date"

option now = () => 2020-02-11T12:21:03.293534940Z

date.monthDay(t: -8d)

// Returns 3
```
