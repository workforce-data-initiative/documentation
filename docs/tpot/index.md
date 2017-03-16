# Training Provider Outcomes Toolkit

The Training Provider Outcomes Toolkit (TPOT) is a collection of tools for
securely collecting, connecting, analyzing, aggregating, and publishing data on
wage and employment outcomes for education and training participants.

State and local workforce development boards aim to improve employment and
workforce investment in their regions.

## Collecting data from training providers

There are many hundreds or thousands of training providers within the purview
of each workforce development board. Each one must securely upload their
participant data to their workforce board in order to be eligible for federal
funds. The resulting aggregate statistics on participant outcomes will be
invaluable marketing materials for successful programs, regardless of federal
funding. This means that the workforce development boards must be equipped to
receive and validate the data.

Training providers range from small trade apprenticeships to community colleges
to multi-state organizations, with a wide range of data sophistication. The
way(s) in which the workforce data board collects participant outcomes must be
easy and accessible to all organizations. At the same time, it must be easy
for the board itself to automatically process and validate the datasets.

### The Data Package

In order to support these use-cases, the toolkit uses the [Data Package]()
specification in order to encapsulate and describe training provider outcome
data in a systematic fashion.

#### Create a Data Package specification

Each workforce development board should create a data package specification
that defines the specific fields and values that they require the training
providers to use.

The [**Data Packagist**](http://datapackagist.okfnlabs.org/) tool allows you to
easily define these packages in the browser. You can also view existing package
specifications with the [online data package
viewer](http://data.okfn.org/tools/view).  Finally, you can validate your
specification with an [online validator](http://data.okfn.org/tools/validate).

### Uploading website

Once a data package specification is created, it may be used to easily
customize a self-hosted website that enables validating and uploading data
packages from training providers. This site is designed to be simple to modify
and setup a custom instance for each training provider. A demo uploading
website is available at [send.dataatwork.org](http://send.dataatwork.org). The
source code is available for customization [on
GitHub](https://github.com/workforce-data-initiative/datapackagist).

### The data warehouse

The upload website is designed to securely upload the data packages to a
data warehouse for each workforce board.  _Stay tuned for updates._

## Data matching

Once the workforce board has collected the training providers' outcomes, it
must link the participant information with wage and employment information from
other departments. In order to facilitate this matching, we have developed an
easy-to-use and open-source deduplication package,
[SuperDeduper](https://github.com/dssg/superdeduper). This allows for a
combination of exact record linkage and probabalistic fuzzy matching in order
to link as many participants as possible to the other datasets.

## Data processing

A [wide variety of tools](http://frictionlessdata.io/tools/) have been
developed that support the Data Package format. It is possible to load your
data package into [many analysis
languages](http://frictionlessdata.io/tools/#libraries) including
[Python](https://github.com/frictionlessdata/datapackage-py) and
[R](https://github.com/frictionlessdata/datapackage-py). It's also possible to
load the data packages into [many database
systems](http://frictionlessdata.io/tools/#use-data-packages-with-) including
[SQL Server](https://github.com/bimlscript/BETDPI) and
[PostgreSQL](https://github.com/okfn/dptools/blob/master/bin/load-postgresql.py)
 . Work is underway to support
[Excel](https://github.com/frictionlessdata/ideas/issues/41) and [Google
Sheets](https://github.com/okfn/data.okfn.org/issues/24).

