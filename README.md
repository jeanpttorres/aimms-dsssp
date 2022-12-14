# aimms-dsssp

# Description

This is a project that runs the Algorithms described in the paper "LP-based Heuristics for the Distinguishing Substring Selection Problem"[1].


# How to Install

This is written for AIMMS and the project should be open under a AIMMS license. The following steps illustrate how to download, install, and setup a valid AIMMS Community License. 

## Download AIMMS

This project is designed for the AIMMS version 4.89.
You can download a compatible AIMMS version on the following url: https://download.aimms.com/aimms/download/data/4.89/4.3/Aimms-4.89.4.3-x64-VS2017.exe

## Generate AIMMS license

You can get your Free Personal Community AIMMS license on the link: https://licensing.cloud.aimms.com/license/community.htm
This license is free to use for personal usage and it comes with a CBC Optimizer license.

AIMMS offers a Student/Academic license with comes with CPLEX. This license can be requested through https://www.aimms.com/support/licensing/academic-license/

Once you have registered for a valid license (Academic or Community), you will receive a e-mail with a personal activation URL.

## Installing AIMMS

### Windows

Execute the Aimms-4.89.4.3-x64-VS2017.exe file and follow the given steps. Once it asks for a license, choose the URL authentication method and fill the correspondent space with the authentication URL you received in the previous step. 

### Linux

TO-DO

# How to Use

* Open the AIMMS Software

* Open the DSSSP Project: File->Open Project

* The system should open on your browser

## Instance Files

There is the option to load an instance file through the page "Input". A sample file can be found at "data/text_input_example.dssp", but the file expects the following structure:

```
n
c f
m
kc kf
a(1)
..
a(n)
sc(1)
sc(2)
...
sc(kc)
sf(1)
sf(2)
...
sf(kf)
```

Where n, c, f, m, kc and kf are integers and their meaning is indicated below:

- n: alphabet size
- c: Sc's cardinality
- f: Sf's cardinality
- m: length of the target string
- kc: parameter used for refining the distances between target string and strings within the Sc set
- kf: parameter used for refining the distances between target string and strings within the Sf set

The values read for a(1) .. a(n) are the symbols (characteres) from the Alphabet.
The string in 'Sc' should be writen in sequence, one in each line. The same structure applies for `Sf`, informed right after the last `Sc` sequence.

# Dummy Execution

* Choose the Input Step and click "+" on the button "Upload TXT". Choose the file located on data/text_input_example.dssp and, after uploading it, click on the button again in order to process the file. 

* Choose the Optimization step and click on the "PLAY" button, on the bottom-right corner. 

# References

[1] Torres, J.P.T., Hoshino, E.A. LP-based heuristics for the distinguishing string and substring selection problems. Ann Oper Res 316, 1205???1234 (2022). https://doi.org/10.1007/s10479-021-04138-5

[2] https://github.com/jeanpttorres/dssp

[3] https://github.com/jeanpttorres/aimms-dsssp
