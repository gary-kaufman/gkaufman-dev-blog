---
date: 2024-09-25
authors:
  - gary-kaufman
categories:
  - Python
  - openpyxl
---

# openpyxl Tips and Tricks

`openpyxl` is a Python library for reading and writing Excel files.
Please check our their full [documentation](https://openpyxl.readthedocs.io/en/stable/#) for more information.
I often use it to format rows or extract data from one Excel file to another. We'll check out various tips with my example below.

<!-- more -->

For today's example we'll have an input file that represents a large membership document. Our goal will be to find out who hasn't been to
class in a while, and in a smaller output file, create a 'roll' for class, highlighting students that have excessive absences.

