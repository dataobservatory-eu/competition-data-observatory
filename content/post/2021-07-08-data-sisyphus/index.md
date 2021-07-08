+++
title = "The Data Sisyphus"
subtitle = ""
date = 2021-07-08T09:00:00
lastmod = 2021-07-08T09:00:00
draft = false

authors = ["daniel_antal"]

tags = ["metadata","data-as-service"]

summary = "Sisyphus was punished by being forced to roll an immense boulder up a hill only for it to roll down every time it neared the top, repeating this action for eternity.  When was a file downloaded from the internet?  What happened with it sense?  Are their updates? Did the bibliographical reference was made for quotations?  Missing values imputed?  Currency translated? Who knows about it – who created a dataset, who contributed to it?  Which is the final, checked, approved by a senior manager? "

projects = ["eu-datathon_2021"]

# Featured image
[image]
  # Caption (optional)
  caption = "Climate Awareness in the Arab World. Get this plot from      [figshare](https://doi.org/10.6084/m9.figshare.14854359)."

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Center"

  # Show image only in page previews?
  preview_only = false

+++

Sisyphus was punished by being forced to roll an immense boulder up a hill only for it to roll down every time it neared the top, repeating this action for eternity.  This is the price that project managers and analysts pay for the inadequate documentation of their data assets.  When was a file downloaded from the internet?  What happened with it sense?  Are their updates? Did the bibliographical reference was made for quotations?  Missing values imputed?  Currency translated? Who knows about it – who created a dataset, who contributed to it?  Which is an intermediate format of a spreadsheet file, and which is the final, checked, approved by a senior manager? 

Data documentation is very boring, and like data processing, when done manually, it can be extremely time consuming.  In the case of small datasets, creating manually the description to a dataset may be more costly in time and wages than the data itself.  But without proper documentation, the data will be very difficult to find, even in your own computer or server, and very difficult to reuse.  As the years pass, the project managers will decide that it is better to download or buy it again; the analyst will rather re-check the currency translations.

<td style="text-align: center;">{{< figure src="/media/img/gems/Uncut-diamond_Edit.jpg" caption="Uncut diamonds need to be cut, polished, and you have to make sure that they come from a legal source. Data is similar: it needs to be tidied up, checked and documented before use." numbered="false" >}}</td>

Data is hardly informative – it may be a page in a book, a file in an obsolete file format on a governmental server, an Excel sheet that you do not remember to have checked for updates.  Most data are useless, because we do not know how it can inform us, or we do not know if we can trust it.  The processing can be a daunting task, not to mention the most boring and often neglected documentation duties after the dataset is final and pronounced error-free by the person in charge of quality control. Data analysts are reported to spend about 80% of their working hours on data processing and not data analysis -- partly, because data processing is a very laborious task and partly because they do not know if the person who sat before them at the same desk has already performed these tasks, or if the person responsible for quality control checked for errors.

> “Data is potential information, analogous to potential energy: work is required to release it.” 

While humans are much better at analysing the information and human agency is required for trustworthy AI, computers are much better at processing and documenting data.  We apply to important concepts to our data service: we always process the data to the tidy format, we create an authoritative copy, and we always automatically add descriptive and processing metadata. 

- [x] The tidy data format means that the data has a uniform and clear data structure and semantics, therefore it can be automatically validated for many common errors and can be automatically documented by either our software or any other professional data science application. It is not as strict as the schema for a relational database, but it is strict enough to make, among other things, importing into a database easy.

- [x] The authoritative copy is held at an independent repository, it has a globally unique identifier that protects you from accidental data loss, mixing up with unfinished an untested version.

- [x] The descriptive metadata contains information on how to find the data, access the data, join it with other data (interoperability) and use it, and reuse it, even years from now. Among others, it contains file format information and intellectual property rights information.

- [x] The processing metadata makes the data usable in strictly regulated professional environments, such as in public administration, law firms, investment consultancies, or in scientific research. We give you the entire processing history of the data, which makes peer-review or external audit much easier and cheaper.

<td style="text-align: center;">{{< figure src="/media/img/gems/Diamond_Polisher.jpg" caption="Cutting the dataset to a format with clear semantics and documenting it with the FAIR metadata concep exponentially increases the value of data. It can be publisehd or sold at a premium." numbered="false" >}}</td>

Metadata is often more valuable and more costly to make than the data itself, yet it remains an elusive concept for senior or financial management.  Metadata is information about how to correctly use the data and has no value without the data itself.  Data acquisition, such as buying from a data vendor, or paying an opinion polling company, or external data consultants appears among the material costs, but metadata is never sold alone, and you do not see its cost.  If the data source is cheap or has a low quality, you do not even get it.  If you do not have it, it will show up as a human resource cost in research (when your analysist or junior researcher are spending countless hours to find out the missing metadata information on the correct use of the data) or in sales costs (when you try to reuse a research, consulting or legal product and you have comb through your archive and retest elements again and again.)