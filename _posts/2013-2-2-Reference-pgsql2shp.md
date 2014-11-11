---
layout: post
title: Reference - pgsql2shp
---



```bash
pgsql2shp -f "/home/lfelling/tmp/shp_export" -h localhost -u postgres -P postgres worh "SELECT label, the_geom FROM place WHERE my_type = 'state'"

```