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

To install the associated R package use install.packages in R:

```
install.packages('rdataretriever')
```

### Command line interface

List available datasets:

```
retriever ls
```

Install a dataset into csv files:

```
retriever install csv iris
```

Install a dataset into an SQLite database named iris.sqlite:

```
retriever install sqlite iris -f iris.sqlite
```

Available install formats are: mysql, postgres, sqlite, access, csv, json, and
xml.

### R interface

List available datasets:

```
retriever::datasets()
```

Install a dataset into sqlite:

```
retriever::install('iris', 'sqlite')
```

Download and load data directly into R:

```
iris_data <- retriever::fetch('iris')
```

See the [documentation](#documentation) for more commands and details.
