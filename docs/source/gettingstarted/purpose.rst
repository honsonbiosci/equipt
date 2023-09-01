Purpose and contents
====================

The goal of equipt is to make quantitative polymerase chain reaction (qPCR) analysis easier, faster, and more reproducible. qPCR instrument software generally has useful tools for calling Ct values and performing melting curve analyses, but it often falls short in using these values for more complicated calculations. These calculations generally require the user to manually label wells in clunky, point-and-click software which is neither convenient nor reproducible.

Most researchers I know use Excel for qPCR analysis, or write custom scripts in Python or R every time they run an experiment. Not only is this tedious, but using Excel for data analysis is [extremely fraught.](https://theconversation.com/excel-autocorrect-errors-still-plague-genetic-research-raising-concerns-over-scientific-rigour-166554#:~:text=Our%20research%20shows%20autocorrect%20errors,gene%20name%20mangled%20by%20autocorrect). 

Equipt solves these problems by:

1) Enforcing a set of standardized layouts for 96- or 384-well plates.

2) Reproducibly labeling wells such that errors are easily detected. 

3) Using these standardizations in modules for common qPCR analyses.

Using equipt will make your qPCR analysis mostly painless and entirely reproducible.

Tools
-----

Currently equipt has four main tools:

* namer : Labels samples, primers, and dilutions (if applicable) on qPCR outputs. Provides a standardized input for all other functions.

* averager : Averages replicates and calculates standard deviation. If desired, avg_filt will remove outliers (specified by a maximum acceptable standard deviation) from groups of replicate wells and report how many wells it excluded from each group of replicate wells.

* efficiency : Calculates qPCR primer efficiency from a standard curve. 

* deltact : Performs ΔCt, ΔΔCt, and/or fold-change analysis for differential gene expression or enrichment analysis.
