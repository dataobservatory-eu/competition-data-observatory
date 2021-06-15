---
title: Open Government Data
summary: Public-sector information re-use and freedom of information
tags:
- psi
- open-gov
- foi
date: "2021-05-16T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

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

In the EU, open data is governed by the [Directive on open data and the re-use of public sector information - in short: Open Data Directive (EU) 2019 / 1024](https://eur-lex.europa.eu/legal-content/EN/TXT/?qid=1561563110433&uri=CELEX:32019L1024). It entered into force on 16 July 2019. It replaces the [Public Sector Information Directive](https://eur-lex.europa.eu/legal-content/en/ALL/?uri=CELEX:32003L0098), also known as the *PSI Directive* which dated from 2003 and was subsequently amended in 2013.

## Is There Value in Open Data?

- Open data is often untapped and provides you competitive advantage in scientific research or market intellgience. Most open data is not publicy accessible, and available upon request.
- Most European open data comes from tax authorities, meteorological offices, managers of transport infrastructure, and other governmental bodies whose data needs are very different from yours.  Their data must be carefully evaluated, re-processed, and if necessary, imputed to be usable for your scientific, business or policy goals.
- The use of open science data is problematic in different ways: usually understanding the data documentation requires domain-specific specialist knowledge.  [Open science data](https://music.dataobservatory.eu/data/open-science/) is even more scattered and difficult to access than technically open, but not public governmental data.

## Why Downloading Does Not Work?

-  Most open data is not available on the internet. 
- If it is available, it is not in a form that you can easily import into a spreadsheet application like Excel or OpenOffice, or into a statistical application like SPSS or STATA.
- Even the data quality of trusted web sources, like the Eurostat website, can be very low. Eurostat just publishes what it gets from governments, and often has no mandate to fix errors.  The data is full with missing information, and in the case of regional statistics, faulty region codes and region names that make matching your data or placing them on a map impossible.
- Adjusting euros with millions of euros, correctly translating dollars to euros, pounds to kilograms requires plenty of work. This is a very error-prone process when done by humans.

## Can Open Data be Used in Machine Learning and AI?

- Most public and open data sources have many missing observations; machine learning models usually cannot hanlde missingness. These points must be carefully imputed with approximations, which can be very challenging when the data has geographical dimension.
- Removing missing values makes samples extremely biased and your model will learn from omissions, not information.

## How We Add Value?

[Our team](https://music.dataobservatory.eu/#contributors) knows how to bring data to the light, and release it in the best possible format with the highest quality documentation.

1. Our curators know the data sources very well, and know what should be acquired, re-processed, and re-documented to your needs.
2. Our developers know how to create reliable, open source statistical software that sends the data through dozens of automated unit-tests, and open their algorithms for peer-review by other computational statisticians.  
3. Our service development team helps to make our high-quality, reprocessed open data available for your workflows in business, science or public policy.
