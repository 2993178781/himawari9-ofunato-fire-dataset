# Ofunato Himawari-9 Subpixel Fire Mapping

This repository provides the processed data and validation materials for the
main positional evaluation of subpixel active-fire mapping in Ofunato,
Iwate Prefecture, Japan, on 21 February 2025.

## Data access

Download the data package from [Release v1.0.0](PUBLISHED_RELEASE_URL).

## Source data

- Himawari-9 Advanced Himawari Imager observations and auxiliary cloud and
  aerosol products are available through the
  [JAXA Himawari Monitor](https://www.eorc.jaxa.jp/ptree/).
- NOAA-21 VIIRS 375 m active-fire detections are available from the
  [NASA FIRMS archive](https://firms.modaps.eosdis.nasa.gov/download/).

The data manifest records the source products, versions, filenames,
observation times, and study area used in the analysis.

## Files

| File | Description |
| --- | --- |
| `data_manifest.csv` | Source products, observation times, and grid information |
| `viirs_reference.csv` | Six VIIRS detections used in the positional evaluation |
| `outputs/` | Prediction files for the proposed method and both baselines |
| `pointwise_distances.csv` | Nearest distances in metres for each reference point and method |

## Reproducing the comparison

Use `ref_id` to link the reference detections and distance records.
For each method, calculate the 90th percentile from the six distances.
At each matching radius, divide the number of reference detections within
that radius by the total number of reference detections. The data manifest
specifies the distance definition and quantile method used in the manuscript.

Third-party satellite products remain subject to their providers' terms of use.
