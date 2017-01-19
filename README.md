# pretty-metric [![Build Status](https://travis-ci.org/stevelacy/pretty-metric.svg?branch=master)](https://travis-ci.org/stevelacy/pretty-metric)

> Parse, convert, and humanize metric sizes

## Install

```shell
$ npm install pretty-metric
```
## Usage

```js

const prettyMetric = require('pretty-metric')

prettyMetric(1500).km()
// => 1.5km

prettyMetric(1500).humanize()
// => 1.5km

prettyMetric(.4).humanize()
// => 40cm

// Using input types
prettyMetric(150).input('cm').humanize()
// => 1.5m

prettyMetric(0.5).input('cm').humanize()
// => 5mm

```

## Functions

#### humanize()
> Converts the input value to a more human recognizable size

```js
prettyMetric(150).humanize()
// => 1.5m

```

#### input()
> Sets the input value to a particular metric

This can be chained with `humanize()`

```js
prettyMetric(1500).input('cm').km()
// => 0.015km

prettyMetric(1500).input('mm').humanize()
// => 1.5m
```

## Supported sizes

```
km:  kilometer  - 1000m
hm:  hectometer - 100m
dam: decameter  - 10m
m:   meter      - 1m
dm:  decimeter  - .1m
cm:  centimeter - .01m
mm:  milimeter  - .001m

```

## [License](LICENSE) (MIT)
