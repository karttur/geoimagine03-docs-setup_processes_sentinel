---
layout: article
title: mgrs-extract_tile_coords_v090.json
categories: setup_processes
excerpt:  Extract mgrs coordinates (NGA original)
tags:: 
    - mgrs-extract_tile_coords
date: 2021-11-08
modified: 2021-11-08
comments: true
share: true
---

# mgrs extract tile coords (setup_processes)

###  Extract mgrs coordinates (NGA original)

The json command file <span class='file'>mgrs-extract_tile_coords_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
      "processid": "extractmgrscoords",
      "dsversion": "3.0",
      "parameters": {
        "centroid": "True"
      },
      "srcpath": {
        "volume": "karttur",
        "hdrfiletype": "shp",
        "datfiletype": "shp"
      },
      "srccomp": {
        "mgrs-100km": {
          "source": "nga",
          "product": "mgrs",
          "folder": "mgrs",
          "band": "mgrs-100km",
          "prefix": "mgrs-100km",
          "suffix": "v1",
          "scalefac": "1",
          "offsetadd": "0",
          "dataunit": "na",
          "celltype": "vector",
          "cellnull": "0",
          "measure": "N",
          "masked": "N"
        }
      }
    }
  }
}
```
