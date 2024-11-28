# stac-browser-docker

This repository builds docker images for [stac-browser](https://github.com/radiantearth/stac-browser/).

## What is stac-browser?
This is a Spatio-Temporal Asset Catalog (STAC) browser for static catalogs. Minimal support for APIs is implemented, but it not the focus of the Browser and may lead to issues. It attempts to surface all included data in a user-centric way (an approach which can inform how data is represented in the evolving spec). It is implemented as a single page application (SPA) for ease of development and to limit the overall number of catalog reads necessary when browsing (as catalogs may be nested and do not necessarily contain references to their parents).

## Flavors
### Plain
Plain image with stac-browser built and static files exposed by nginx
### With prefix
Same image as before, but with `pathPrefix` set to `/browser/`. See [stac-browser docs](https://github.com/radiantearth/stac-browser/tree/main?tab=readme-ov-file#create-a-custom-image) for details.

## Update policy
It runs on CRON daily and builds `latest` based on `main` branch, and an image for the latest tag if there are any changes.