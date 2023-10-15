---
title: fmtree
tags: [fmtree, Web, Python]
---

# fmtree

> A python package for parsing file system (or any tree like structure) and output a custom format such as markdown table of content.


[PyPi](https://pypi.org/project/fmtree/)

[GitHub](https://github.com/fmtree-dev/fmtree)

## Usage

```bash
pip install fmtree
```

## Features

- Parse file system
- Filter file system with custom filter
  - MarkdownFilter
  - ExtensionFilter
- Output file system with custom format
  - TreeCommandFormatter
  - GithubMarkdownContentFormatter

```
# TreeCommandFormatter
OSCP
└── Notes
    ├── Tools
    │   ├── Python.md
    │   ├── nmap.md
    │   ├── Netcat.md
    │   └── Metasploit.md
    ├── common.md
    ├── FileTransfer.md
    ├── README.md
    ├── Service.md
    └── Bash.md
```

```python
import sys
import pathlib2
from fmtree.core.scraper import Scraper
from fmtree.core.format import TreeCommandFormatter, GithubMarkdownContentFormatter
from fmtree.core.filter import MarkdownFilter
from fmtree.core.sorter import Sorter


path_ = pathlib2.Path('/OSCP')
scraper = Scraper(path_, scrape_now=False, keep_empty_dir=False)

# add filter
scraper.add_filter(filter_=MarkdownFilter())

# run scraper
scraper.run()

# GNU Tree Format
formatter = TreeCommandFormatter(scraper.get_tree())
stringio = formatter.generate()
print(stringio.getvalue())

# sort
sorter_ = Sorter()
tree = sorter_(scraper.get_tree())

# GitHub Content Format
formatter = GithubMarkdownContentFormatter(tree)
stringio = formatter.generate()
print(stringio.getvalue())
formatter.to_stream(sys.stdout)
```