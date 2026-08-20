# Drone Datasets

Public datasets for drone workflows, curated and tested: raw photogrammetry image sets,
aerial imagery, LiDAR and point clouds, and detection benchmarks. Every dataset here can
be processed with the skills in [drone-skills](https://github.com/neblihq/drone-skills).

**The bar for this catalog: we downloaded it and processed it ourselves.** Every entry
states what it contains, how big it is, its license as the source states it, and what we
ran it through. Dead links and datasets nobody here has actually opened do not get listed.

## Contents

- [Photogrammetry Image Sets](#photogrammetry-image-sets)
- [Orthomosaics and Mapping](#orthomosaics-and-mapping)
- [LiDAR and Point Clouds](#lidar-and-point-clouds)
- [Detection and Tracking](#detection-and-tracking)

## Photogrammetry Image Sets

- **[Sheffield Cross](https://github.com/pierotofy/drone_dataset_sheffield_cross)** —
  172 geotagged JPGs (4000×3000, DJI Phantom 3 Professional) from a single 22-minute
  flight at 62 m AGL over Sheffield Cross, Palm Harbor, Florida (April 2018), plus a GCP
  file (3 surveyed points measured across 24 images, UTM 17N). ~889 MB. All 172 images
  verified intact.
  - License, verbatim from the repo's
    [LICENSE](https://github.com/pierotofy/drone_dataset_sheffield_cross/blob/master/LICENSE):
    "This is free and unencumbered software released into the public domain." (The Unlicense)
  - Tested 2026-08-20 with
    [orthomosaic-processing](https://github.com/neblihq/drone-skills/tree/main/orthomosaic-processing)
    (OpenDroneMap via Docker, `opendronemap/odm:gpu` with `--dsm`): 172/172 images
    reconstructed in 11m36s on an RTX 5080 workstation. Outputs: orthomosaic GeoTIFF
    5040×4123 at 5.0 cm/px (WGS 84 / UTM 17N), DSM GeoTIFF, 126 MB georeferenced .laz
    point cloud, and a textured mesh. Working directory grew from 849 MB to 13 GB during
    processing. The GCP file was not used in this run.

## Orthomosaics and Mapping

*First entries in testing.*

## LiDAR and Point Clouds

*Coming.*

## Detection and Tracking

*Coming.*

## Contributing

Suggestions welcome by issue or pull request. An entry needs: what the dataset contains in
one line, approximate size, the license verbatim from the source, and what you processed
it with. Links only; this repo never rehosts data.

## Related

- [awesome-drone-ai](https://github.com/neblihq/awesome-drone-ai): a curated list of AI
  skills, agents, and workflows for drone pilots.
- [drone-skills](https://github.com/neblihq/drone-skills): Claude skills these datasets
  can be processed with.

---

Curated by [Nebli](https://nebli.ai).
