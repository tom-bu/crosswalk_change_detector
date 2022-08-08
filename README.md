
# Towards HD Map Updates with Crosswalk Change Detection From Vehicle-Mounted Cmaeras
1. [Crosswalk Detector](crosswalk_detector)
2. [BEV Change Detector](bev_change_detector)
3. [Busedge](busedge)


## Overview


Many autonomous vehicles rely on high-definition maps that contain road layout and road semantics as priors for perception, planning and prediction. However, these maps can become stale over time as the road environment changes. This thesis develops a road monitoring framework that allows for automatic change detection of crosswalks with a cost-effective sensor suite of vehicle-mounted cameras and GPS data. Furthermore, this thesis explores using an edge computer on a commercial bus to receive and analyze live data captured in Pittsburgh.

## Crosswalk Detector
Public datasets are often limited, biased, and fixed in size. This portion trains a detector on the mapillary vistas dataset and allows for further bootstrapping with locally collected data. 

## BEV Change Detector
This portion presents a method that maps detections from 2D images onto a ground plane by using multi-view geometry and 3D reconstructions of the scene.  With this method, detections from multiple frames can be accumulated in the bird's-eye-view to better represent an intersection, and consistency checks can be performed to remove false detections.

## BusEdge
This portion explores using the crosswalk change detector in an edge-computing enabled commuter bus that has active cameras. With GPS locations of existing crosswalk intersections, the bus can send relevant images for the crosswalk change detector to analyze. 


## Citations
Please cite the following thesis if you find this useful.
  ```
  @mastersthesis{Bu-crosswalk-change,
  author = {Tom Bu},
  title = {Towards HD Map Updates with Crosswalk Change Detection from Vehicle-Mounted Cameras},
  year = {2022},
  month = {August},
  school = {},
  address = {Pittsburgh, PA},
  number = {CMU-RI-TR-22-34},
  }
  ```

## License

- All original source code and documentation are licensed under the
  [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.html).
- Some configuration and trivial data files are licensed under CC0-1.0.
- Non-original source files were Apache-2.0, BSD-3-Clause, BSD-2-Clause, or MIT
  licensed and retain their original licensing.

A copy of all licenses is provided in the `LICENSES/` folder, it is possible to
create a bill of materials, which licenses various files use, with a tool like
[reuse](https://reuse.software).