+++
title = "How We Add Value to Public Data With Imputation and Forecasting?"
subtitle = ""
date = 2021-11-08T10:00:00+01:00
lastmod = 2021-11-09T11:00:00+01:00
draft = false

authors = ["daniel_antal"]

tags = ["music","data-as-service", "API", "metadata"]

summary = "Public data sources are often plagued by missng values. Naively you may think that you can ignore them, but think twice: in most cases, missing data in a table is not missing information, just malformatted information which will destroy your beautiful visualization or stop your application from working. In this example we show how we increase the usable subset of a public dataset by 66.7%, which is a deal-breaker in panel regressions or machine learning (AI) solutions."

projects = ""

# Featured image
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Center"

  # Show image only in page previews?
  preview_only = true

+++

Public data sources are often plagued by missng values. Naively you may think that you can ignore them, but think twice: in most cases, missing data in a table is not missing information, just malformatted information. Once you want to make a beautiful chart, or use them in a business forecasting model, a machine learning (AI) applicaton or a more complex scientifc model, this approach will stop you.  Any good-looking  visualization, or machine learning model, or complex scientific model will need complete datasets, and naively discarding missing data points is wasting too much information. In this example we are continuing the example a not-so-easy to find public dataset.

<td style="text-align: center;">{{< figure src="/media/img/blogposts_2021/jack-sloop-eYwn81sPkJ8-unsplash.jpg" caption="In the previous blogpost we explained how we added value with documenting the data following the *FAIR* principle and with the professional curatorial work of placing the data in context, and linking it to other information sources that are not depending on the English language, and can connect our radio dataset to other data, books, publications, regardless if they are described in English, or in German, Portugese or Croatian Photo: [Jack Sloop](https://unsplash.com/photos/eYwn81sPkJ8)." numbered="false" >}}</td>

Completing the missing datapoints requires statistical production information (why the data may be missing?) and data science knowhow (how to impute the missing value.) If you do not have a good statistician or data scientist in your team, you will need high-quality, complete datasets. This is what our automated data observatories provide.

## Why is data missing?

International organization offer many statistical products, but usually they are on an ‘as-is’ basis. For example, Eurostat is the world’s premiere statistical agency, but it has no right to overrule whatever data the member states of the European Union, and some other cooperating European countries give to them. And they cannot force these countries to hand over data if they fail to do so. As a result, there will be many data points that are missing, and often data points that have a wrong (obsolete) description or geographical dimensions. We will show the geographical aspect of the problem in a separate blogpost, we now only focus on the missing data.

Some countries have only recently started providing data to the Eurostat umbrella organization, and it is likely that you will find few datapoints for North Macedonia or Bosnia-Herzegovina. Other countries provide data with some delay, and the last one or two years are missing. And there are gaps in some counties’ data, too.

<td style="text-align: center;">{{< figure src="/media/img/blogposts_2021/trb_plot.png" caption="See the authoritative copy of the [dataset](https://zenodo.org/record/5652118#.YYkhVmDMKUk)." numbered="false" >}}</td>

This is a headache if you want to use the data in some machine learning (AI) application or in a multiple or panel regression model. You can, of course, discard countries or years where you do not have full data coverage, but this approach usually wastes too much information--if you work with 12 years, and only one data point is missing, you would be discarding an entire country’s 11-years’ worth of data. Another option is to estimate the values, or otherwise impute the missing data, when this is possible with reasonable precision. This is where things get tricky, and you will likely need a statistician or a data scientist on board.

## What can we improve?

Consider that the data is only missing from one year for a particular country, 2015.  The naive solution would be to omit 2015 or the country at hand from the dataset. This is pretty destructive, because we know a lot about the radio market turnover in this country and in this year! But leaving 2015 blank will not look good on a chart, and will make your machine learning application or your regression model stop.

A statistician or a radio market expert will tell you that you know more-or-less the missing information: the total turnover was certainly not zero in that year.  With some statistical or radio domain-specific knowledge you will use the 2014, or 2016 value, or a combination of the two and keep the country and year in the dataset.

Our improved dataset added backcasted (using the best time series model fitting the country's actually present data), forecasted (again, using the best time series model), and approximated data (using linear approximation.) In a few cases, we add the last or next known value.  To give a few quantiative indicators about our work:

- Increased number of observations: 65%
- Reduced missing values: -48.1%
- Increased non-missing subset for regression or AI: +66.67%

If your organization is working with panel (longitudional multiple) regressions or various machine learning (AI) applications, then your team knows that the +66.67% is usually a deal-breaker in the choice of models and punctuality of estimates or KPIs or other quantiative products.  And that they would spent about 90% of their data analyst (data scientist) resources on achieving this +66.67% usability.

If you happen to work in an NGO, a business unit or a research institute that does not employ data scientists, then it is likely that you can never achieve this improvement, and you have to give up on a number of quantiative tools or visualizations.  If you  have a data scientist on board, that professional can start our work as a starting point.  

## Can you trust our data?

We believe that you can trust our data better than the original public source. We use statistical expertise to find out why data may be missing. Often, it is just present in a woring place (for example, the name of a region changed.)

If you are reluctant to use estimates, think about discarding known actual data from your forecast or visualization, because one data point is missing.  How do you provide a more accurate information? By hiding known actual data, because one point is missing, or using all known data and an estimate?

Our codebooks and our API uses the [Statistical Data and Metadata eXchange](https://sdmx.org/?page_id=3215/) documentation standards to clearly indicate which data is observed, which is missing, which is estimated, and of course, also how it is estimated. 
This example highlights another important aspect of data trustworthiness. If you have a better idea, you can replace them with a better estimate.  

Our indicators come with standardized codebooks that do not only contain the descriptive metadata, but administrative metadata about the history of the indicator values. You will find very important information about the statistical method we used the fill in the data gaps, and even link the reliable, the peer-reviewed scientific, statistical software that made the calculations. For data scientists, we record the plenty of information about the computing environment, too-–this can come handy if you our estimates need external authentication, or you suspect a bug.

## Avoid the data sisyphus

If you work in an academic institution, in an NGO or a consultancy, you can never be sure who downloaded the [Annual detailed enterprise statistics for services (NACE Rev. 2 H-N and S95)](https://appsso.eurostat.ec.europa.eu/nui/show.do?dataset=sbs_na_1a_se_r2&lang=en) Eurostat folder from Eurostat. If they have modified the Excel table. Did they already make corrections with the missing data? What method did they use? To prevent the many potential problems, you will likely download it again, and again, and again...

<td style="text-align: center;">{{< figure src="/media/img/blogposts_2021/Sisyphus_Bodleian_Library.png" caption="See our [The Data Sisyphus](https://reprex.nl/post/2021-07-08-data-sisyphus/) blogpost." numbered="false" >}}</td>

We have a better solution. You can always rely on our API to import directly the latest, best data, but if you want to be sure, you can use our [regular backups](https://zenodo.org/record/5652118#.YYhGOGDMLIU) on Zendo. Zenodo is an open science repository managed by CERN and supported by the European Union. On Zenodo, you can find an authoritative copy of our indicator (and its previous versions) with a digital object identifier, in  this case, [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5652118.svg)](https://doi.org/10.5281/zenodo.5652118). These datasets will be preserved for decades, and nobody can manipulate them. You cannot accidentally overwrite them, and we have no backdoor to modify them.

*Are you a data user? Give us some feedback? Shall we do some further
automatic data enhancements with our datasets? Document with different
metadata? Link more information for business, policy, or academic use? Please 
give us any [feedback](https://reprex.nl/#contact)!*
