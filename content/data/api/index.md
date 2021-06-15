---
title: API
summary: Get data from the Economy Data Observatory via our API
tags:
- api
date: "2021-06-01T11:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

authors:
- daniel_antal
- botond_vitos

image:
  caption: 
  focal_point: Smart

links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/EconDataObs
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

Our observatory has a new data API which allows access to our daily refreshing open data. You can access the API via [api.economy.dataobservatory.eu](http://api.economy.dataobservatory.eu/) (*apologies for the ugly, temporary subdomain masking!*).

All the data and the metadata are available as open data, without database use restrictions, under the [ODbL](https://opendatacommons.org/licenses/odbl/) license.


## Indicator table {#indicator-table}

The indicator table contains the actual values, and the various estimated/imputed values of the indicator, clearly marking missing values, too.

{{< figure src="/media/img/observatory_screenshots/EDO_API_indicator_table.png" caption="api.economy.dataobservatory.eu: indicator retrieval" numbered="true" >}}

You can get the data in [CSV](http://52.4.54.69/database/indicator.csv?_size=max) or [json](http://52.4.54.69/database/indicator.json) format, or write SQL querries. (Tutorials in SQL, R, Python will be posted shortly.)

## Description metadata table {#description-table}

The [description table](http://52.4.54.69/database/description) contains the actual values, and the various estimated/imputed values of the indicator, clearly marking missing values, too. 

{{< figure src="/media/img/observatory_screenshots/EDO_API_indicator_table.png" caption="api.economy.dataobservatory.eu: descriptive metadata" numbered="true" >}}

## Labelling table {#labelling-table}

The [labelling table](http://52.4.54.69/database/labelling) contains the way we have handled labels, codes and unit information from the original source. One of the reasons why open data is so hard to use for analysts is the many measurement unit and currencly translations that needs to be made when downloading them from an often not well-documented source. Our API contains data that is ready to be joined with your data, or our other indicators, because these unit and currency translations are made consistently and explicitly.

{{< figure src="/media/img/observatory_screenshots/EDO_API_labelling_table.png" caption="api.economy.dataobservatory.eu: labelling and unit information" numbered="true" >}}

## Processing Metadata table {#metadata-table}

The [metadata table](http://52.4.54.69/database/metadata) contains various data processing information, such as the first and last actual observation of the indicator, the number of approximated, forecasted, backcasted values, last update at source and in our system, and so on. 

{{< figure src="/media/img/observatory_screenshots/EDO_API_metadata_table.png" caption="api.economy.dataobservatory.eu: processing metadata" numbered="true" >}}

