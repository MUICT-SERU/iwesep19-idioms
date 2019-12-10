## Visualizing the Usage and Evolution of Pythonic Idioms Over Time: A Case Study of ‘the with open’ Idiom

## [Home](https://muict-seru.github.io/iwesep19-idioms/) | [Experiment]()


## Experimental Set Up

### 1.Data Collection

1.1 Prepare Query

Non-idiomatic
```markdown
open = (‘file.txt’)
```
Idiomatic
```markdown
with open(‘file.txt’) as f:
```
1.2 Use the queries to search on searchcode.com, website for searching source code repositories by giving a code query,
 to find data sets to use in the experiment

### 2.Data Preparation

Use CCGrep, pattern matching detection tool with non-file name relying, to extract the occurrences of Idiomatic Python code and Non-idiomatic code in the projects.

IMAGE HERE


## Studied Projects

1. Beaker: an open source software for managing and automating labs of test computers.

2. DFHack: a Dwarf Fortress memory access library, distributed with a wide variety of useful scripts and plugins.

3. iPython: a command shell for interactive computing in multiple programming languages originally developed for Python.

4. Tshock: a toolbox for Terraria servers and communities


TABLE HERE


