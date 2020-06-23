---
date: 2020-03-11
title: Datendownload 
categories: opensensemap
description: Datendownload über die openSenseMap
type: Document
resources:
image1: /images/2020-03-11-opensensemap-download/1-filter-en.png
image2: /images/2020-03-11-opensensemap-download/1-download-en.png
---

There are several possibilities to download sensor data from the openSenseMap.
Depending on the problem, one option is available for each.
The data recorded by the senseBox is Open Data, i.e. it is freely available to all users. 

## Data of one box

An archive for all measurements in the openSenseMap database is kept under <https://archive.opensensemap.org>.
Here, measured values structured by tag and box are available as CSV or ZIP archives.

## Filter

By clicking on the tab "Filter" in the openSenseMap you can optionally have specific things pre-filtered for your search and the subsequent download of the data.
If you filter by a name, you can also download the values of a single senseBox.
You can see that the filter is active by a red triangle under the "Name" tab
{% include image.html image=page.image1 %}

## Graphical representation of data  

In addition to the filter function, you can also view the statistics of each box by simply clicking on any box on the map.
## Download

If you select the "Data Download" tab on the openSenseMap, you can apply a number of spatial and temporal filters to the values already measured by the senseBoxes.

{% include image.html image=page.image2 %}


### Select period

First you should select a period of time from which you would like to have the data displayed.
This can be done manually or you can choose between "last 24 hours", "Last week" or "Last month".  


### Group by...

Now you select whether you want to have the data averaged. Here you can again select a time period.
Alternatively, it is also possible to have the raw data output.

### Operation

Under "Operation" you can decide which function you want to apply to the values.
For example, you can calculate the maximum or minimum of measured temperatures.

### Select a sensor

Here you can now select a sensor from which you want to have the desired values displayed with the filters you selected before.

### Columns

Click on the "Columns" button to choose what additional information you would like to receive about your values.


> **Attention**: Depending on the selection of the filter parameters the download can be very large (several 100MB)!


### Formats

Currently, only the CSV data format is supported, which can be used with spreadsheet tools such as 
Microsoft Excel, Libre office, R-Studio or ArcGis.

Each line contains a measurement of a senseBox with the selected phenomenon.
The measured value (`value`), location of the sensor (`lat`, `lng`, reference system WGS84) and a time stamp (`createdAt`) are given in one column each:

```csv
createdAt;value;lat;lng
2016-09-20T10:05:49.581Z;18.70;7.64568;51.962372
2016-09-20T10:00:52.689Z;18.62;7.64568;51.962372
2016-09-20T09:55:54.282Z;18.47;7.64568;51.962372
....
```

## API-Download

If the two options mentioned above are not flexible enough, complex requests can be made via the [REST API under `/boxes/data`](osem_api.md#get-latest-measurements-for-a-phenomenon-as-csv-).

The command line tool `curl` is useful for such requests.
Open a terminal under Linux and enter the following command to download all temperature measurements in the geographical area 51°N - 52°N, 7°E - 8°E into the file `measurements.csv`:

```
curl "https://api.opensensemap.org/boxes/data?phenomenon=Temperatur&bbox=7,51,8,52" > measurements.csv
```

Other suitable parameters (period, Box-IDs, ...) can be found in the linked API documentation.