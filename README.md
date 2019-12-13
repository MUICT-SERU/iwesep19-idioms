# Visualizing the Usage and Evolution of Pythonic Idioms Over Time: A Case Study of ‘the with open’ Idiom


Tattiya Sakulniwat∗, Raula Gaikovina Kula†, Chaiyong Ragkhitwetsagul∗,Morakot Choetkiertikul∗, Thanwadee Sunetnanta∗, Dong Wang†, Takashi Ishio†and Kenichi Matsumoto†

*Faculty of Information and Communication Technology (ICT), Mahidol University

†Nara Institute of Science and Technology (NAIST)

Email: tattiya.sakul@gmail.com,{chaiyong.rag, morakot.cho, thanwadee.sun}@mahidol.ac.th{raula-k, wang.dong.vt8, ishio, matumoto}@is.naist.jp



## Introduction

### Pythonic Idioms

Pythonic is defined in python.org glossary part as the code which closely follows the most common idioms of the Python language.
Idioms, generally, defined as a phrase that have particular meaning that cannot be directly translate from each word.
Put them together, Pythonic Idiom is is the way to write a set of code to execute particular function by following the principle of Python language.


The idiomatic way of writing code would help on increase efficiency of the code as following figure:

![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/Compare.png?raw=true)



### Why Python?

- Python  programming  language  ranks  in  the  top  three  most  used  by programmers due to [rank by GitHub](https://octoverse.github.com/projects#languages)
- Stack Overflow predicts that it will be the most used in 2020.
- The most active repository on GitHub is “TensorFlow” and it uses Python.

### Why 'with open' statement?

|           Idioms           | # Projects |  Total count  |
|:--------------------------:|:----------:|:-------------:|
|    List   comprehension    |     866    |     75,466    |
|     with      statement    |     848    |    143,453    |
|          Decorator         |     765    |    114,545    |

This table is referenced from the paper [On the Usage of Pythonic Idioms](https://www.zora.uzh.ch/id/eprint/156901/1/paper.pdf)
The data is collected from 1000 example projects in GitHub repository. The collumn numver of projects represents the number of projects that use following Pythonic idiom. Total count means the total number of occurrences of each idiom all over the whole project.


The ‘with open’ is in the 2nd rank but it has the highest number of occurrences so it is selected as the case study of this research.


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

![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/da%20final.png?raw=true)


## Studied Projects

1. Beaker: an open source software for managing and automating labs of test computers.

2. DFHack: a Dwarf Fortress memory access library, distributed with a wide variety of useful scripts and plugins.

3. iPython: a command shell for interactive computing in multiple programming languages originally developed for Python.

4. Tshock: a toolbox for Terraria servers and communities

|    Project    |    Releases    |    Contributors    |    Start   Date    |    End   Date    |
|:-------------:|:--------------:|:------------------:|--------------------|------------------|
|     Beaker    |       432      |         63         |    12/08/2006      |    21/05/2019    |
|     DFHack    |       123      |         112        |    24/02/2010      |    28/12/2018    |
|    iPython    |       94       |         608        |    14/09/2008      |    03/07/2019    |
|    TShock     |    70          |    62              |    03/06/2013      |    01/04/2019    |


## Result

### Research Question 1: Do developers adopt the idiom for file reading statements over time?

Answer: We found that 3 out of the 4 selected projects adopt the with open idiom. However, the amount of adoption differs. One project only contains the idiom without the non-idiomatic counterpart. The other two projects have non-idiomatic code more at the beginning and idiomatic code more from the middle to the last release. 


The scatter plot graphs below show the occurrence of Idiomatic and NOn-idiomatic codes through time. The red dot represents the occurrence of Non-idiomatic code and the green dots represents the Idiomatic one. X-axis adopts date of development of the code and Y-axis is for package name hosted in the project.


#### Project: Beaker
![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/BeakerG1.jpg?raw=true)


#### Project: TShock
![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/TShockG1.jpg?raw=true)

#### Project: DFHack
![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/DFHackG1.jpg?raw=true)

#### Project: iPython
![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/IPythonG1.jpg?raw=true)

### Research Question 2: Do the developers fix their non-idiomatic file reading statements?

Answer: We found that two projects (Beaker and DFHack) contain removals of non-idiomatic code along with the inclusions of the with open idiom.  Nonetheless, there are some projects that also introduce more non-idiomatic file reading statements (TShock and IPython).


Each project has two bar graphs visualizing the number of usage of both Idiomatic and Non-idiomatic codes in each file of the project. The red bar stands for Non-idiomatic code usage and the green bar is for Idiomatic code usage. X-axis represents each file name in the whole project while Y-axis shows the number of time both style of codes occur.


#### Project: Beaker
![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/BeakerG2A.jpg?raw=true)
![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/BeakerG2B.jpg?raw=true)

#### Project: TShock
![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/TShockG2A.jpg?raw=true)
![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/TShockG2B.jpg?raw=true)

#### Project: DFHack
![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/DFHackG2A.jpg?raw=true)
![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/DFHackG2B.jpg?raw=true)

#### Project: iPython
![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/iPythonG2A.jpg?raw=true)
![figure1](https://github.com/MUICT-SERU/iwesep19-idioms/blob/master/figure/iPythonG2B.jpg?raw=true)


## Further Information
Full paper: https://muict-seru.github.io/files/iwesep19_Tattiya.pdf


More of SERU publications!: https://muict-seru.github.io/publications.html
     
