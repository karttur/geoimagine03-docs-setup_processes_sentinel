---
layout: article
title: regions-sentineltiles_v090.json
categories: setup_processes
excerpt:  Link default regions to sentinel tiles
tags:: 
    - regions-sentineltiles
date: 2021-11-08
modified: 2021-11-08
comments: true
share: true
---

# regions sentineltiles (setup_processes)

###  Link default regions to sentinel tiles

The json command file <span class='file'>regions-sentineltiles_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "regionssentinel": {
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
      "processid": "LinkDefaultRegionsToSentinel",
      "version": "3.0",
      "parameters": null,
      "overwrite": "N",
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
          "suffix": "global"
        }
      }
    }
  }
}
```
