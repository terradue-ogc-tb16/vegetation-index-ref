# Vegetation index

## About this Jupyter Notebook

This notebook takes as input a Sentinel-2 STAC catalog containing a single item and accesses the red, nir, swir16 and swir22 assets to derive the three normalized differences:

- NDVI = (nir - red) / (nir + red)
- NDWI = (nir - swir16) / (nir + swir16)
- NBR = (nir - swir22) / (nir + swir22)

The notebook writes the results as a self-contained STAC catalog with local assets described as bands with new common names ndvi, ndwi and nbr.

## Running this notebook

### Using Binder

Click on the badge below to run this notebook on Binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gl/terradue-ogctb16%2Feoap%2Fd169-jupyter-nb%2Fvegetation-index/master?urlpath=lab)

### Using docker

Clone the repository with:

```bash
git clone https://gitlab.com/terradue-ogctb16/eoap/d169-jupyter-nb/vegetation-index.git

cd vegetation-index
```

Build the docker image:

```bash
docker-compose build
```

This step may take a few minutes as during the build process the base Docker is downloaded and a new docker image is created. 

Run the application with:

```bash
docker-compose up
```

Use your browser to open the URL 127.0.0.1:9005 or 0.0.0.0:9005

