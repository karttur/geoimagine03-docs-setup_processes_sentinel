---
layout: article
title: sentinel-extract_tile_coords_v090.json
categories: setup_processes
excerpt:  Extract sentinel coordinates
tags:: 
    - sentinel-extract_tile_coords
date: 2021-11-08
modified: 2021-11-08
comments: true
share: true
---

# sentinel extract tile coords (setup_processes)

###  Extract sentinel coordinates

The json command file <span class='file'>sentinel-extract_tile_coords_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "organize": {
    "userproj": {
      "userid": "karttur",
      "projectid": "karttur",
      "tractid": "karttur",
      "siteid": "*",
      "plotid": "*",
      "system": "sentinel"
    },
    "period": {
      "timestep": "static"
    },
    "process": {
      "processid": "extractsentineltilecoords",
      "dsversion": "3.0",
      "parameters": {
        "centroid": "False"
      },
      "srcpath": {
        "volume": "karttur",
        "hdrfiletype": "shp",
        "datfiletype": "shp"
      },
      "srccomp": {
        "sentinel-tiles": {
          "source": "ESA",
          "product": "sentineltiles",
          "folder": "mgrs",
          "band": "sentinel-tiles",
          "prefix": "sentinel-tiles",
          "suffix": "global",
          "system": "ancillary"
        }
      }
    }
  }
}
```
