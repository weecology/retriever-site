---
title: "Quick Start"
bg: blue  #defined in _config.yml, can use html color like '#0fbfcf'
color: white   #text color
fa-icon: rocket
---

The Data Retriever is written in Python and run using a command line interface
or an associated R package. It installs publicly available data into a variety
of databases (MySQL, PostgreSQL, SQLite, MS Access) and file formats (csv, json,
xml).

### Installation

If you have Python installed use pip from the terminal
([additional install instructions](#install)):

```
pip install retriever
```

or install using conda:

```
conda install retriever -c conda-forge
```

To install the associated R package:

```
install.packages('rdataretriever')
```

### Command line interface

List available datasets:

```
retriever ls
```

Install the [Portal dataset](https://github.com/weecology/portaldata) into csv
files:

```
retriever install csv portal
```

Install the [iris dataset](https://archive.ics.uci.edu/ml/datasets/Iris/) into
an SQLite database named iris.sqlite:

```
retriever install sqlite iris -f iris.sqlite
```

Available install formats are: mysql, postgres, sqlite, access, csv, json, and
xml.

### R interface

List available datasets:

```
rdataretriever::datasets()
```

Install the [iris dataset](https://archive.ics.uci.edu/ml/datasets/Iris/) into
SQLite:

```
rdataretriever::install('iris', 'sqlite')
```

Download and load
[data on forest fires](https://archive.ics.uci.edu/ml/datasets/Forest+Fires)
directly into R:

```
iris_data <- rdataretriever::fetch('iris')
```

See the [documentation](#docs) for more commands, details, and
datasets.
