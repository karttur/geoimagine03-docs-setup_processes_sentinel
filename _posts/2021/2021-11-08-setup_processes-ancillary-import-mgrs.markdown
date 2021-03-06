---
layout: article
title: ancillary-import-mgrs_v090.json
categories: setup_processes
excerpt:  Import NGA projections (UTM and MGRS)
tags:: 
    - ancillary-import-mgrs
date: 2021-11-08
modified: 2021-11-08
comments: true
share: true
---

# ancillary import mgrs (setup_processes)

###  Import NGA projections (UTM and MGRS)

The json command file <span class='file'>ancillary-import-mgrs_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
        "orgid": "NGA",
        "dsname": "mgrs",
        "dsversion": "1.0",
        "accessdate": "20180831",
        "copyright": "",
        "regionid": "globe",
        "regioncat": "globe",
        "dataurl": "http://earth-info.nga.mil/GandG/coordsys/grids/universal_grid_system.html",
        "metaurl": "http://earth-info.nga.mil/GandG/coordsys/grids/universal_grid_system.html",
        "title": "mgrs global tiles",
        "label": "mgrs global tiles"
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
          "utm-zones": {
            "datadir": "data/NGA/UTM_Zone_Boundaries",
            "datafile": "UTM_Zone_Boundaries",
            "datalayer": "UTM_Zone_Boundaries",
            "title": "UTM zone boundaries",
            "label": "UTM zone boundaries"
          }
        },
        {
          "gdz-zones": {
            "datadir": "data/NGA/MGRS_GZD_WorldWide",
            "datafile": "MGRS_GZD_WorldWide",
            "datalayer": "MGRS_GZD_WorldWide",
            "title": "MGRS Grid Zone Designator",
            "label": "MGRS Grid Zone Designator"
          }
        },
        {
          "mgrs-100km-land": {
            "datadir": "data/NGA/NGA_mgrs_100km_polys",
            "datafile": "NGA_mgrs_100km_polys",
            "datalayer": "NGA_mgrs_100km_polys",
            "title": "MGRS 100km square for land",
            "label": "MGRS 100km square for land"
          }
        },
        {
          "mgrs-100km": {
            "datadir": "data/NGA/mgrs_100km_polys",
            "datafile": "mgrs_100km_polys",
            "theme": "support",
            "subtheme": "tiles",
            "metadir": "",
            "metadfile": "",
            "title": "MGRS 100km square (global)",
            "label": "MGRS 100km square (global)"
          }
        }
      ],
      "dstcomp": [
        {
          "utm-zones": {
            "source": "nga",
            "product": "projection",
            "content": "utm",
            "layerid": "utm-zones",
            "prefix": "utm-zones",
            "suffix": "0",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "0",
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "gdz-zones": {
            "source": "nga",
            "product": "mgrs",
            "content": "mgrs",
            "layerid": "gdz-zones",
            "prefix": "gdz-zones",
            "suffix": "v1",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "0",
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "mgrs-100km-land": {
            "source": "nga",
            "product": "mgrs",
            "content": "mgrs",
            "layerid": "mgrs-100km-land",
            "prefix": "mgrs-100km-land",
            "suffix": "v1",
            "dataunit": "boundary",
            "celltype": "vector",
            "cellnull": "0",
            "measure": "N",
            "masked": "N"
          }
        },
        {
          "mgrs-100km": {
            "source": "nga",
            "product": "mgrs",
            "content": "mgrs",
            "layerid": "mgrs-100km",
            "prefix": "mgrs-100km",
            "suffix": "v1",
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
