# Extension of CoverageJSON terms

## Terms for prefix: metocean

### metocean:level

Type: number

The height above ground for a meteorological measurement instrument, in meters (m).

### metocean:standard_name

Type: string

The standard name for the observed property as listed in the CF convention.

### metocean:measurementType

Type: object

Identical to the object for the property `measurementType` in OGC API - Environmental Data Retrieval v1.2, with the following schema:

```yaml
type: object
title: Parameter measurement approach
description: Approach to calculating the data values
required:
  - method
properties:
  method:
    type: string
    examples: 
      - mean
  duration:
    type: string
    title: Measurement time duration
    description: The time duration that the value was calculated for as an RFC3339
       duration value.  If the method value is instantaneous this value is
       not required.
    examples: 
      - PT10M
```

## Examples
 
```json
{
  "type": "CoverageCollection",
  "coverages": [
    {
      "type": "Coverage",
      "domain": {
        "type": "Domain",
        "domainType": "PointSeries",
        "axes": {
          "x": {
            "values": [
              17.83117
            ]
          },
          "y": {
            "values": [
              69.6005
            ]
          },
          "t": {
            "values": [
              "2025-12-05T04:00:00Z",
              "2025-12-05T08:00:00Z",
              "2025-12-05T08:10:00Z",
              "2025-12-05T08:30:00Z",
              "2025-12-05T08:40:00Z",
              "2025-12-05T08:50:00Z",
              "2025-12-05T09:00:00Z",
              "2025-12-05T09:10:00Z",
              "2025-12-05T09:20:00Z",
              "2025-12-05T09:30:00Z",
              "2025-12-05T09:40:00Z",
              "2025-12-05T09:50:00Z",
              "2025-12-05T10:00:00Z",
              "2025-12-05T10:10:00Z",
              "2025-12-05T10:20:00Z",
              "2025-12-05T10:30:00Z",
              "2025-12-05T10:40:00Z",
              "2025-12-05T10:50:00Z",
              "2025-12-05T11:00:00Z",
              "2025-12-05T11:10:00Z",
              "2025-12-05T11:20:00Z",
              "2025-12-05T11:30:00Z",
              "2025-12-05T11:40:00Z",
              "2025-12-05T11:50:00Z",
              "2025-12-05T12:00:00Z",
              "2025-12-05T12:10:00Z",
              "2025-12-05T12:20:00Z",
              "2025-12-05T12:30:00Z",
              "2025-12-05T12:40:00Z",
              "2025-12-05T12:50:00Z",
              "2025-12-05T13:00:00Z",
              "2025-12-05T13:10:00Z",
              "2025-12-05T13:20:00Z"
            ]
          }
        },
        "referencing": [
          {
            "coordinates": [
              "x",
              "y"
            ],
            "system": {
              "type": "GeographicCRS",
              "id": "http://www.opengis.net/def/crs/OGC/1.3/CRS84"
            }
          },
          {
            "coordinates": [
              "t"
            ],
            "system": {
              "type": "TemporalRS",
              "calendar": "Gregorian"
            }
          }
        ]
      },
      "parameters": {
        "wind_from_direction:10.0:point:PT0S": {
          "type": "Parameter",
          "description": {
            "en": "Wind from direction at 10.0m, aggregated over PT0S with method 'point'"
          },
          "observedProperty": {
            "id": "https://vocab.nerc.ac.uk/standard_name/wind_from_direction",
            "label": {
              "en": "Wind from direction"
            }
          },
          "unit": {
            "label": {
              "en": "deg"
            },
            "symbol": {
              "value": "°",
              "type": "https://qudt.org/vocab/unit/DEG"
            }
          },
          "metocean:measurementType": {
            "method": "point",
            "duration": "PT0S"
          },
          "metocean:standard_name": "wind_from_direction",
          "metocean:level": 10.0
        },
        "wind_speed:10.0:point:PT0S": {
          "type": "Parameter",
          "description": {
            "en": "Wind speed at 10.0m, aggregated over PT0S with method 'point'"
          },
          "observedProperty": {
            "id": "https://vocab.nerc.ac.uk/standard_name/wind_speed",
            "label": {
              "en": "Wind speed"
            }
          },
          "unit": {
            "label": {
              "en": "m/s"
            },
            "symbol": {
              "value": "m/s",
              "type": "https://qudt.org/vocab/unit/M-PER-SEC"
            }
          },
          "metocean:measurementType": {
            "method": "point",
            "duration": "PT0S"
          },
          "metocean:standard_name": "wind_speed",
          "metocean:level": 10.0
        },
        "wind_speed_of_gust:10.0:maximum:PT10M": {
          "type": "Parameter",
          "description": {
            "en": "Wind speed of gust at 10.0m, aggregated over PT10M with method 'maximum'"
          },
          "observedProperty": {
            "id": "https://vocab.nerc.ac.uk/standard_name/wind_speed_of_gust",
            "label": {
              "en": "Wind speed of gust"
            }
          },
          "unit": {
            "label": {
              "en": "m/s"
            },
            "symbol": {
              "value": "m/s",
              "type": "https://qudt.org/vocab/unit/M-PER-SEC"
            }
          },
          "metocean:measurementType": {
            "method": "maximum",
            "duration": "PT10M"
          },
          "metocean:standard_name": "wind_speed_of_gust",
          "metocean:level": 10.0
        }
      },
      "ranges": {
        "wind_from_direction:10.0:point:PT0S": {
          "type": "NdArray",
          "dataType": "float",
          "axisNames": [
            "t",
            "x",
            "y"
          ],
          "shape": [
            33,
            1,
            1
          ],
          "values": [
            148.0,
            143.0,
            148.0,
            146.0,
            148.0,
            150.0,
            148.0,
            146.0,
            152.0,
            152.0,
            148.0,
            148.0,
            158.0,
            162.0,
            161.0,
            153.0,
            152.0,
            153.0,
            153.0,
            149.0,
            150.0,
            149.0,
            151.0,
            149.0,
            144.0,
            141.0,
            144.0,
            145.0,
            144.0,
            146.0,
            145.0,
            148.0,
            149.0
          ]
        },
        "wind_speed:10.0:point:PT0S": {
          "type": "NdArray",
          "dataType": "float",
          "axisNames": [
            "t",
            "x",
            "y"
          ],
          "shape": [
            33,
            1,
            1
          ],
          "values": [
            6.19999981,
            5.0,
            5.5,
            6.4000001,
            6.4000001,
            6.69999981,
            6.4000001,
            6.30000019,
            5.80000019,
            6.19999981,
            5.9000001,
            6.4000001,
            5.80000019,
            5.80000019,
            5.4000001,
            6.0,
            6.4000001,
            6.19999981,
            5.80000019,
            5.80000019,
            6.0999999,
            6.5999999,
            6.5,
            6.5,
            6.69999981,
            6.5999999,
            6.80000019,
            6.69999981,
            6.4000001,
            6.4000001,
            6.5999999,
            6.4000001,
            6.5
          ]
        },
        "wind_speed_of_gust:10.0:maximum:PT10M": {
          "type": "NdArray",
          "dataType": "float",
          "axisNames": [
            "t",
            "x",
            "y"
          ],
          "shape": [
            33,
            1,
            1
          ],
          "values": [
            8.0,
            6.69999981,
            7.0999999,
            8.0,
            7.9000001,
            8.0,
            7.5,
            7.80000019,
            7.4000001,
            8.39999962,
            7.69999981,
            7.5999999,
            7.9000001,
            8.39999962,
            7.80000019,
            8.39999962,
            8.10000038,
            7.5,
            7.69999981,
            7.5999999,
            7.80000019,
            8.30000019,
            7.9000001,
            7.80000019,
            8.10000038,
            8.10000038,
            8.30000019,
            8.30000019,
            7.69999981,
            8.10000038,
            7.5999999,
            8.10000038,
            8.0
          ]
        }
      },
      "metocean:wigosId": "0-20000-0-01015"
    },
    {
      "type": "Coverage",
      "domain": {
        "type": "Domain",
        "domainType": "PointSeries",
        "axes": {
          "x": {
            "values": [
              17.83117
            ]
          },
          "y": {
            "values": [
              69.6005
            ]
          },
          "t": {
            "values": [
              "2025-12-05T04:00:00Z",
              "2025-12-05T08:00:00Z",
              "2025-12-05T09:00:00Z",
              "2025-12-05T10:00:00Z",
              "2025-12-05T11:00:00Z",
              "2025-12-05T12:00:00Z",
              "2025-12-05T13:00:00Z"
            ]
          }
        },
        "referencing": [
          {
            "coordinates": [
              "x",
              "y"
            ],
            "system": {
              "type": "GeographicCRS",
              "id": "http://www.opengis.net/def/crs/OGC/1.3/CRS84"
            }
          },
          {
            "coordinates": [
              "t"
            ],
            "system": {
              "type": "TemporalRS",
              "calendar": "Gregorian"
            }
          }
        ]
      },
      "parameters": {
        "air_temperature:2.0:maximum:PT1H": {
          "type": "Parameter",
          "description": {
            "en": "Air temperature at 2.0m, aggregated over PT1H with method 'maximum'"
          },
          "observedProperty": {
            "id": "https://vocab.nerc.ac.uk/standard_name/air_temperature",
            "label": {
              "en": "Air temperature"
            }
          },
          "unit": {
            "label": {
              "en": "Cel"
            },
            "symbol": {
              "value": "°C",
              "type": "https://qudt.org/vocab/unit/DEG_C"
            }
          },
          "metocean:measurementType": {
            "method": "maximum",
            "duration": "PT1H"
          },
          "metocean:standard_name": "air_temperature",
          "metocean:level": 2.0
        },
        "air_temperature:2.0:minimum:PT1H": {
          "type": "Parameter",
          "description": {
            "en": "Air temperature at 2.0m, aggregated over PT1H with method 'minimum'"
          },
          "observedProperty": {
            "id": "https://vocab.nerc.ac.uk/standard_name/air_temperature",
            "label": {
              "en": "Air temperature"
            }
          },
          "unit": {
            "label": {
              "en": "Cel"
            },
            "symbol": {
              "value": "°C",
              "type": "https://qudt.org/vocab/unit/DEG_C"
            }
          },
          "metocean:measurementType": {
            "method": "minimum",
            "duration": "PT1H"
          },
          "metocean:standard_name": "air_temperature",
          "metocean:level": 2.0
        },
        "air_temperature:2.0:point:PT0S": {
          "type": "Parameter",
          "description": {
            "en": "Air temperature at 2.0m, aggregated over PT0S with method 'point'"
          },
          "observedProperty": {
            "id": "https://vocab.nerc.ac.uk/standard_name/air_temperature",
            "label": {
              "en": "Air temperature"
            }
          },
          "unit": {
            "label": {
              "en": "Cel"
            },
            "symbol": {
              "value": "°C",
              "type": "https://qudt.org/vocab/unit/DEG_C"
            }
          },
          "metocean:measurementType": {
            "method": "point",
            "duration": "PT0S"
          },
          "metocean:standard_name": "air_temperature",
          "metocean:level": 2.0
        },
        "relative_humidity:2.0:point:PT0S": {
          "type": "Parameter",
          "description": {
            "en": "Relative humidity at 2.0m, aggregated over PT0S with method 'point'"
          },
          "observedProperty": {
            "id": "https://vocab.nerc.ac.uk/standard_name/relative_humidity",
            "label": {
              "en": "Relative humidity"
            }
          },
          "unit": {
            "label": {
              "en": "%"
            },
            "symbol": {
              "value": "%",
              "type": "https://qudt.org/vocab/unit/PERCENT"
            }
          },
          "metocean:measurementType": {
            "method": "point",
            "duration": "PT0S"
          },
          "metocean:standard_name": "relative_humidity",
          "metocean:level": 2.0
        },
        "wind_from_direction:10.0:maximum:PT1H": {
          "type": "Parameter",
          "description": {
            "en": "Wind from direction at 10.0m, aggregated over PT1H with method 'maximum'"
          },
          "observedProperty": {
            "id": "https://vocab.nerc.ac.uk/standard_name/wind_from_direction",
            "label": {
              "en": "Wind from direction"
            }
          },
          "unit": {
            "label": {
              "en": "deg"
            },
            "symbol": {
              "value": "°",
              "type": "https://qudt.org/vocab/unit/DEG"
            }
          },
          "metocean:measurementType": {
            "method": "maximum",
            "duration": "PT1H"
          },
          "metocean:standard_name": "wind_from_direction",
          "metocean:level": 10.0
        },
        "wind_speed:10.0:maximum:PT1H": {
          "type": "Parameter",
          "description": {
            "en": "Wind speed at 10.0m, aggregated over PT1H with method 'maximum'"
          },
          "observedProperty": {
            "id": "https://vocab.nerc.ac.uk/standard_name/wind_speed",
            "label": {
              "en": "Wind speed"
            }
          },
          "unit": {
            "label": {
              "en": "m/s"
            },
            "symbol": {
              "value": "m/s",
              "type": "https://qudt.org/vocab/unit/M-PER-SEC"
            }
          },
          "metocean:measurementType": {
            "method": "maximum",
            "duration": "PT1H"
          },
          "metocean:standard_name": "wind_speed",
          "metocean:level": 10.0
        },
        "wind_speed_of_gust:10.0:maximum:PT1H": {
          "type": "Parameter",
          "description": {
            "en": "Wind speed of gust at 10.0m, aggregated over PT1H with method 'maximum'"
          },
          "observedProperty": {
            "id": "https://vocab.nerc.ac.uk/standard_name/wind_speed_of_gust",
            "label": {
              "en": "Wind speed of gust"
            }
          },
          "unit": {
            "label": {
              "en": "m/s"
            },
            "symbol": {
              "value": "m/s",
              "type": "https://qudt.org/vocab/unit/M-PER-SEC"
            }
          },
          "metocean:measurementType": {
            "method": "maximum",
            "duration": "PT1H"
          },
          "metocean:standard_name": "wind_speed_of_gust",
          "metocean:level": 10.0
        }
      },
      "ranges": {
        "air_temperature:2.0:maximum:PT1H": {
          "type": "NdArray",
          "dataType": "float",
          "axisNames": [
            "t",
            "x",
            "y"
          ],
          "shape": [
            7,
            1,
            1
          ],
          "values": [
            1.39999998,
            1.5,
            1.60000002,
            1.5,
            1.5,
            1.39999998,
            1.39999998
          ]
        },
        "air_temperature:2.0:minimum:PT1H": {
          "type": "NdArray",
          "dataType": "float",
          "axisNames": [
            "t",
            "x",
            "y"
          ],
          "shape": [
            7,
            1,
            1
          ],
          "values": [
            1.20000005,
            1.29999995,
            1.29999995,
            1.39999998,
            1.29999995,
            1.29999995,
            1.29999995
          ]
        },
        "air_temperature:2.0:point:PT0S": {
          "type": "NdArray",
          "dataType": "float",
          "axisNames": [
            "t",
            "x",
            "y"
          ],
          "shape": [
            7,
            1,
            1
          ],
          "values": [
            1.29999995,
            1.5,
            1.39999998,
            1.39999998,
            1.39999998,
            1.39999998,
            1.39999998
          ]
        },
        "relative_humidity:2.0:point:PT0S": {
          "type": "NdArray",
          "dataType": "float",
          "axisNames": [
            "t",
            "x",
            "y"
          ],
          "shape": [
            7,
            1,
            1
          ],
          "values": [
            74.0,
            72.0,
            72.0,
            71.0,
            70.0,
            73.0,
            72.0
          ]
        },
        "wind_from_direction:10.0:maximum:PT1H": {
          "type": "NdArray",
          "dataType": "float",
          "axisNames": [
            "t",
            "x",
            "y"
          ],
          "shape": [
            7,
            1,
            1
          ],
          "values": [
            144.0,
            143.0,
            149.0,
            148.0,
            151.0,
            144.0,
            146.0
          ]
        },
        "wind_speed:10.0:maximum:PT1H": {
          "type": "NdArray",
          "dataType": "float",
          "axisNames": [
            "t",
            "x",
            "y"
          ],
          "shape": [
            7,
            1,
            1
          ],
          "values": [
            6.80000019,
            5.30000019,
            6.80000019,
            6.5,
            6.5999999,
            6.69999981,
            6.9000001
          ]
        },
        "wind_speed_of_gust:10.0:maximum:PT1H": {
          "type": "NdArray",
          "dataType": "float",
          "axisNames": [
            "t",
            "x",
            "y"
          ],
          "shape": [
            7,
            1,
            1
          ],
          "values": [
            9.0,
            7.30000019,
            8.0,
            8.39999962,
            8.39999962,
            8.30000019,
            8.30000019
          ]
        }
      },
      "metocean:wigosId": "0-20000-0-01015"
    }
  ],
  "parameters": {
    "air_temperature:2.0:maximum:PT1H": {
      "type": "Parameter",
      "description": {
        "en": "Air temperature at 2.0m, aggregated over PT1H with method 'maximum'"
      },
      "observedProperty": {
        "id": "https://vocab.nerc.ac.uk/standard_name/air_temperature",
        "label": {
          "en": "Air temperature"
        }
      },
      "unit": {
        "label": {
          "en": "Cel"
        },
        "symbol": {
          "value": "°C",
          "type": "https://qudt.org/vocab/unit/DEG_C"
        }
      },
      "metocean:measurementType": {
        "method": "maximum",
        "duration": "PT1H"
      },
      "metocean:standard_name": "air_temperature",
      "metocean:level": 2.0
    },
    "air_temperature:2.0:minimum:PT1H": {
      "type": "Parameter",
      "description": {
        "en": "Air temperature at 2.0m, aggregated over PT1H with method 'minimum'"
      },
      "observedProperty": {
        "id": "https://vocab.nerc.ac.uk/standard_name/air_temperature",
        "label": {
          "en": "Air temperature"
        }
      },
      "unit": {
        "label": {
          "en": "Cel"
        },
        "symbol": {
          "value": "°C",
          "type": "https://qudt.org/vocab/unit/DEG_C"
        }
      },
      "metocean:measurementType": {
        "method": "minimum",
        "duration": "PT1H"
      },
      "metocean:standard_name": "air_temperature",
      "metocean:level": 2.0
    },
    "air_temperature:2.0:point:PT0S": {
      "type": "Parameter",
      "description": {
        "en": "Air temperature at 2.0m, aggregated over PT0S with method 'point'"
      },
      "observedProperty": {
        "id": "https://vocab.nerc.ac.uk/standard_name/air_temperature",
        "label": {
          "en": "Air temperature"
        }
      },
      "unit": {
        "label": {
          "en": "Cel"
        },
        "symbol": {
          "value": "°C",
          "type": "https://qudt.org/vocab/unit/DEG_C"
        }
      },
      "metocean:measurementType": {
        "method": "point",
        "duration": "PT0S"
      },
      "metocean:standard_name": "air_temperature",
      "metocean:level": 2.0
    },
    "relative_humidity:2.0:point:PT0S": {
      "type": "Parameter",
      "description": {
        "en": "Relative humidity at 2.0m, aggregated over PT0S with method 'point'"
      },
      "observedProperty": {
        "id": "https://vocab.nerc.ac.uk/standard_name/relative_humidity",
        "label": {
          "en": "Relative humidity"
        }
      },
      "unit": {
        "label": {
          "en": "%"
        },
        "symbol": {
          "value": "%",
          "type": "https://qudt.org/vocab/unit/PERCENT"
        }
      },
      "metocean:measurementType": {
        "method": "point",
        "duration": "PT0S"
      },
      "metocean:standard_name": "relative_humidity",
      "metocean:level": 2.0
    },
    "wind_from_direction:10.0:maximum:PT1H": {
      "type": "Parameter",
      "description": {
        "en": "Wind from direction at 10.0m, aggregated over PT1H with method 'maximum'"
      },
      "observedProperty": {
        "id": "https://vocab.nerc.ac.uk/standard_name/wind_from_direction",
        "label": {
          "en": "Wind from direction"
        }
      },
      "unit": {
        "label": {
          "en": "deg"
        },
        "symbol": {
          "value": "°",
          "type": "https://qudt.org/vocab/unit/DEG"
        }
      },
      "metocean:measurementType": {
        "method": "maximum",
        "duration": "PT1H"
      },
      "metocean:standard_name": "wind_from_direction",
      "metocean:level": 10.0
    },
    "wind_from_direction:10.0:point:PT0S": {
      "type": "Parameter",
      "description": {
        "en": "Wind from direction at 10.0m, aggregated over PT0S with method 'point'"
      },
      "observedProperty": {
        "id": "https://vocab.nerc.ac.uk/standard_name/wind_from_direction",
        "label": {
          "en": "Wind from direction"
        }
      },
      "unit": {
        "label": {
          "en": "deg"
        },
        "symbol": {
          "value": "°",
          "type": "https://qudt.org/vocab/unit/DEG"
        }
      },
      "metocean:measurementType": {
        "method": "point",
        "duration": "PT0S"
      },
      "metocean:standard_name": "wind_from_direction",
      "metocean:level": 10.0
    },
    "wind_speed:10.0:maximum:PT1H": {
      "type": "Parameter",
      "description": {
        "en": "Wind speed at 10.0m, aggregated over PT1H with method 'maximum'"
      },
      "observedProperty": {
        "id": "https://vocab.nerc.ac.uk/standard_name/wind_speed",
        "label": {
          "en": "Wind speed"
        }
      },
      "unit": {
        "label": {
          "en": "m/s"
        },
        "symbol": {
          "value": "m/s",
          "type": "https://qudt.org/vocab/unit/M-PER-SEC"
        }
      },
      "metocean:measurementType": {
        "method": "maximum",
        "duration": "PT1H"
      },
      "metocean:standard_name": "wind_speed",
      "metocean:level": 10.0
    },
    "wind_speed:10.0:point:PT0S": {
      "type": "Parameter",
      "description": {
        "en": "Wind speed at 10.0m, aggregated over PT0S with method 'point'"
      },
      "observedProperty": {
        "id": "https://vocab.nerc.ac.uk/standard_name/wind_speed",
        "label": {
          "en": "Wind speed"
        }
      },
      "unit": {
        "label": {
          "en": "m/s"
        },
        "symbol": {
          "value": "m/s",
          "type": "https://qudt.org/vocab/unit/M-PER-SEC"
        }
      },
      "metocean:measurementType": {
        "method": "point",
        "duration": "PT0S"
      },
      "metocean:standard_name": "wind_speed",
      "metocean:level": 10.0
    },
    "wind_speed_of_gust:10.0:maximum:PT10M": {
      "type": "Parameter",
      "description": {
        "en": "Wind speed of gust at 10.0m, aggregated over PT10M with method 'maximum'"
      },
      "observedProperty": {
        "id": "https://vocab.nerc.ac.uk/standard_name/wind_speed_of_gust",
        "label": {
          "en": "Wind speed of gust"
        }
      },
      "unit": {
        "label": {
          "en": "m/s"
        },
        "symbol": {
          "value": "m/s",
          "type": "https://qudt.org/vocab/unit/M-PER-SEC"
        }
      },
      "metocean:measurementType": {
        "method": "maximum",
        "duration": "PT10M"
      },
      "metocean:standard_name": "wind_speed_of_gust",
      "metocean:level": 10.0
    },
    "wind_speed_of_gust:10.0:maximum:PT1H": {
      "type": "Parameter",
      "description": {
        "en": "Wind speed of gust at 10.0m, aggregated over PT1H with method 'maximum'"
      },
      "observedProperty": {
        "id": "https://vocab.nerc.ac.uk/standard_name/wind_speed_of_gust",
        "label": {
          "en": "Wind speed of gust"
        }
      },
      "unit": {
        "label": {
          "en": "m/s"
        },
        "symbol": {
          "value": "m/s",
          "type": "https://qudt.org/vocab/unit/M-PER-SEC"
        }
      },
      "metocean:measurementType": {
        "method": "maximum",
        "duration": "PT1H"
      },
      "metocean:standard_name": "wind_speed_of_gust",
      "metocean:level": 10.0
    }
  }
}
```




