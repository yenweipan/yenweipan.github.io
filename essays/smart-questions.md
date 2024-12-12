---
layout: essay
type: essay
title: "Use Gsutil to download NWM forcing and results"
# All dates must be YYYY-MM-DD format!
date: 2024-12-01
published: true
labels:
  - Qsutil
  - NWM
---

[The National Water Model (NWM)](https://water.noaa.gov/about/nwm) is a hydrologic modeling framework that simulates observed streamflow and complements official National Weather Service (NWS) river forecasts across the U.S., particularly produces guidance at locations that has no traditional river forecast. In the past, it is very difficult to access any NOAA archives. However, thanks to the [NOAA Open Data Dissemination (NODD) program](https://www.noaa.gov/information-technology/open-data-dissemination), a great number of NOAA data are now online cooperating with Amazon Web Services, Google, and Microsoft Azure. I found archived NWM outputs on [Google Cloud](https://console.cloud.google.com/storage/browser/national-water-model?pageState=(%22StorageObjectListTable%22:(%22f%22:%22%255B%255D%22)). It's super to have the archive, but the next question came in: **How am I going to bulk download? I don't want to click folders by folders and download files by files.**

Fortunately, Google provides the [Google Cloud Command Line Interface (gcloud CLI)](https://cloud.google.com/sdk/docs/install-sdk), and the way to use it is very similar to how we use the shell. You just need to install the latest gcloud CLI with the selected system following their [guide](https://cloud.google.com/sdk/docs/install-sdk#windows). Then, you can start using it!