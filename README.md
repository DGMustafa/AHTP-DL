# AHTP-DL
This repository contains the python code and the datasets used to produce the results of the research article titled "Boosted Prediction of Antihypertensive Peptides using Deep Learning".

Data Sets
=========

allseq.csv 

All raw peptide sequences of benchmarking dataset in Fasta format.

fet_all_0.csv 		

Dipeptide Composition (DPC) features with Gap 0 for benchmarking dataset.

fet_all_1.csv 		

DPC features with Gap 1 for benchmarking dataset.

fet_all_2.csv 		

DPC features with Gap 2 for benchmarking dataset.

fet_all_3.csv 		

DPC features with Gap 3 for benchmarking dataset.


allseq_ind.csv 		

All raw peptide sequences of independent dataset in Fasta format.

zero_ind.csv 		

DPC features with Gap 0 for benchmarking dataset.

one_ind.csv 		

DPC features with Gap 1 for benchmarking dataset.

two_ind.csv 		

DPC features with Gap 2 for benchmarking dataset.

three_ind.csv 		

DPC features with Gap 3 for benchmarking dataset.


Python Code
===========

Python code files and their usage is elaborated in this section.


DPC-G-Gap.ipynb 	
---------------
Thid code is used to calculate and prepare g-gap DPC features as described below.

	1. Open DPC.ipynb file and run each cell one by one and follow the instructions written in cell.
	2. After calculation of DPC features with gap 0,1,2,3 the four files will be generated in the current dorectory. 
	3. Open these files one by one and remove first row and first column from each file for further training.


Training on Benchmarking Dataset.ipynb
--------------------------------------
Thid code is used to train on bechmarking dataset once the g-gap DPC features have been generated.  


In Training on Benchmarking Dataset.ipynb, run each cell one by one and follow the instructions written in cells. As a output there are four CNN models for each of four models there are 10 models (Because we have performed 10-fold Cross Validation) and SVM model (final predictor) and it also have 10 models.

Testing on Independent Dataset.ipynb
------------------------------------
This code is used for testing on the independent dataset. In Testing on Independent Dataset.ipynb, run each cell one by one and follow the instructions written in cells.


Test.ipynb
----------
This code is used to test the classifier on the new dataset. In Test.ipynb, run each cell one by one and follow the instructions written in cells.
