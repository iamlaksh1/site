---
title: "Writing an efficient code for GeoPandas and Shapely in 2023"
date: "2023-05-02"
tags:
  - "community"
  - "python"
  - "talks"
  - "teaching"
  - "geopandas"
---

With the release of Shapely 2.0, the GeoPandas-based code that have been optimised years ago may no longer provide the best performance. The workshop organised during the GeoPython 2023 together with Joris van den Bossche showed how to change that and write efficient and convenient GeoPandas code that uses the benefits of the latest developments in the Python geospatial ecosystem.

Workshop resources are available on [Github](https://github.com/martinfleis/efficient-geopandas-workshop).

## Annotation

The Python geospatial ecosystem is constantly evolving, rushing towards better usability, new features, fewer bugs and increasing performance. As a result, the code that might have been optimised a few years ago may not provide the ideal experience today. Such a shift has recently happened in the GeoPandas world. After years of development, Shapely 2.0, a major refactoring of the famous Python wrapper of GEOS, came out in December 2022, switching the way how we think about vector geometry handling. From former scalar geometries requiring for-loops to go through, we can now interact with arrays of them in a performant vectorised manner. These developments directly affect how GeoPandas shall be used, which are the good practices and which are no longer up to speed.

This workshop will walk you through some more and some less common cases of GeoPandas-based code that was efficient prior to the Shapely 2.0 release but is behind today. We will explain what was happening under the hood before vs what is going on now, show you how to refactor your code to use the benefits of Shapely 2.0 and explain the best practices of working with GeoPandas in a way that is both convenient and performant. You can expect solutions for the easy tasks as well as deeper dives into advanced topics all the way to tips on how to write custom code that may be faster than GeoPandas itself.
