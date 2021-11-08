---
layout: article
title: ancillary-import-sentinel_tiles_v090.json
categories: setup_processes
excerpt:  Import sentinel tile system
tags:: 
    - ancillary-import-sentinel_tiles
date: 2021-11-08
modified: 2021-11-08
comments: true
share: true
---

# ancillary import sentinel tiles (setup_processes)

###  Import sentinel tile system

The json command file <span class='file'>ancillary-import-sentinel_tiles_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "ancillary"
  },
  "period": {
    "timestep": "static"
  },
  "process": [
    {
      "processid": "OrganizeAncillary",
      "overwrite": false,
      "parameters": {
        "importcode": "shp",
        "epsg": "4326",
        "orgid": "ESA",
        "dsname": "sentinel",
        "dsversion": "1.0",
        "accessdate": "20180608",
        "copyright": "",
        "regionid": "globe",
        "regioncat": "globe",
        "dataurl": "",
        "metaurl": "",
        "title": "Sentinel global tiles",
        "label": "Sentinel global tiles"
      },
      "srcpath": {
        "volume": ".",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "geoinfo2021",
        "hdr": "shp",
        "dat": "shp"
      },
      "srcraw": [
        {
          "sentinel-product-region": {
            "datadir": "data",
            "datafile": "sentinel_2a",
            "datalayer": "sentinel_2a",
            "title": "Sentinel product region",
            "label": "Sentinel product region"
          }
        },
        {
          "sentinel-tiles": {
            "datadir": "data/ESA/sentinel-tiles-poly",
            "datafile": "sentinel-tiles-poly_sentineltiles_global_0_v1",
            "datalayer": "sentinel-tiles-poly_sentineltiles_global_0_v1",
            "title": "Sentinel global tiles",
            "label": "Sentinel global tiles (polygons)"
          }
        }
      ],
      "dstcomp": [
        {
          "sentinel-product-region": {
            "source": "ESA",
            "product": "sentineltiles",
            "content": "mgrs",
            "layerid": "sentinel-product-region",
            "prefix": "sentinel-product-region",
            "suffix": "v1",
            "dataunit": "na",
            "celltype": "vector",
            "cellnull": "0",
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "sentinel-tiles": {
            "source": "ESA",
            "product": "sentineltiles",
            "content": "mgrs",
            "layerid": "sentinel-tiles",
            "prefix": "sentinel-tiles",
            "suffix": "global",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "0",
            "measure": "N",
            "masked": "N"
          }
        }
      ]
    }
  ]
}
```
