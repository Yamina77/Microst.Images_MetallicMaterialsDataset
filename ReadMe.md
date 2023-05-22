data-publishing-template
========================

There is a step by step guide available <a href="http://training.theodi.org/resources/ODIDataTemplate.pdf" target="_blank">here</a>.

Provides a template for publishing a high quality open dataset. Each repository is designed to host a single dataset, consisting of one or more files.

To create a dataset with open data certificate

1) Fork the <a href="https://github.com/theodi/data-publishing-template" target="_blank">template repository</a> and rename the repository to something more akin to the dataset you will be publishing. This can be done from the respositories settings menu. At the same time re-enable issues from the same screen.

2) Upload <b>data files</b> into the <b>data/</b> directory.

3) For each file uploaded you need to add a <b>.data</b> file in the data directory that specifies the metadata for the file, this file should look like the examples and contain the following fields. Note that the category <b>must not</b> be changed from data.

```
category: data
filename: filename.csv
weight: 2
title: June 2014
description: Transactions in June 2014
type: text/csv
```

Key:

```
weight: The position that the file is displayed on the page, 1 being first.

type: The IANA mime type of the file, e.g. text/csv, application/json etc.
```

4) Edit <b>_config.yml</b> and fill in all the values that describe this dataset, changing the examples

5) Point <b>certificates.theodi.org</b> at the front page of the site and let it automatically fill in values (then add the embed code to _config.yml)

6) Note that many of the certificate fields can be filled in by using the github features that are available under the "Data quality and accuracy" sections.


To customise the look and feel of your dataset site
===================================================

1) Replace logo.png in the img directory with your own company logo

2) edit css/style.css to change colour schemes of the site.

Additional sexiness
===================

The <a href="http://theodi.org" target="_blank">Open Data Institute</a> Github Data publisher automatically produces the following:

* A webpage to host a dataset containing full embedded dcat metadata conforming to <a href="https://theodi.org/guides/marking-up-your-dataset-with-dcat" target="_blank">this best practice guideline</a>.

* A datapackage.json file corresponding to the <a href="https://okfn.org/" target="_blank">Open Knowledge</a> guideline for producing a <a href="http://dataprotocols.org/tabular-data-package/" target="_blank">tabular data package</a>.
