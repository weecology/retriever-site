---
title: "Quick Start"
bg: blue  #defined in _config.yml, can use html color like '#0fbfcf'
color: white   #text color
fa-icon: rocket
---

### Installation

If you have Python installed use `pip` from the terminal:

```
pip install retriever
```

To install the associated R package use `install.packages` in R:

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

Install a dataset into an SQLite database:

```
retriever install sqlite iris -f iris.sqlite
```

### R interface

List available datasets:

```
retriever::datasets()
```

Install a dataset into sqlite:

```
retriever::install('iris', 'sqlite')
```

Download and fetch data directly into R:

```
iris_data <- retriever::fetch('iris')
```
