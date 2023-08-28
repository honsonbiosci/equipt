Purpose and contents
====================

Quipt is a collection of tools for analyzing quantitative PCR data. Why use quipt? The software associated with many qPCR thermocyclers often contains analysis tools. Some functions such as Ct calling and melting curve analysis rely on the raw fluorometric measurements and are practically identical for every experiment. As such, it makes sense for the instrument-associated software to perform these calculations.

After these values are calculated, however, the analysis must be highly specific to the experiment. qPCR machine software usually solves the problem with a point and click approach to labeling wells which is tedious and not reproducible. As such, I know hardly anyone who uses those tools. Instead, most people take their Ct values to Excel, `where errors are frequent and difficult to detect.<https://theconversation.com/excel-autocorrect-errors-still-plague-genetic-research-raising-concerns-over-scientific-rigour-166554#:~:text=Our%20research%20shows%20autocorrect%20errors,gene%20name%20mangled%20by%20autocorrect.>`_

Quipt solves these problems by:

1) Enforcing a set of standardized layouts for 96- or 384-well plates.

2) Reproducibly labeling wells such that errors are easily detected. 

3) Having explicit, user-specified definitions of outliers for dropping replicate wells.

4) Leveraging the above standardizations in functions for common qPCR analyses.

Using quipt will make your qPCR analysis mostly painless and entirely reproducible.

Tools
-----

Currently quipt has four main tools:

* namer : Labels samples, primers, and dilutions (if applicable) on qPCR outputs. Provides a standardized input for all other functions.

* avg_filt : Averages replicates and calculates standard deviation. If desired, avg_filt will remove outliers (specified by a maximum acceptable standard deviation) from groups of replicate wells and report how many wells it excluded from each group of replicate wells.

* efficiency : Calculates qPCR primer efficiency from a standard curve. 

* deltact : Performs ΔCt, ΔΔCt, and/or fold-change analysis for differential gene expression or enrichment analysis.
