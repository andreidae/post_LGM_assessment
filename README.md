Supplementary data for
# Strong and lasting impacts of past global warming on baleen whales and their prey

*Andrea A. Cabrera, Elena Schall, Martine Bérubé, Pia Anderwald, Lutz Bachmann, Simon Berrow, Peter B. Best, Phillip J. Clapham, Haydée A. Cunha, Luciano Dalla Rosa, Carolina Dias, Kenneth P. Findlay, Tore Haug, Mads Peter Heide-Jørgensen, Rus Hoelzel, Kit M. Kovacs, Scott Landry, Finn Larsen, Xênia Moreira Lopes, Christian Lydersen, David K. Mattila, Tom Oosting, Richard M. Pace III, Chiara Papetti, Angeliki Paspati, Luis A. Pastene, Rui Prieto, Christian Ramp, Jooke Robbins, Richard Sears, Eduardo R. Secchi, Mónica A. Silva, Malene Simon, Gísli Víkingsson, Øystein Wiig, Nils Øien and Per J. Palsbøll* 



## Folders
### - 1.Samples_MtDNA_sequences_information
	
An excel file (.xlsx) with the sample ID, mitochondrial DNA sequence, ocean basin and source for each sample and species included in this study
	
### - 2.Migrate-BaleenWhale_InputOutput
	
For each baleen whale species, the input file for MIGRATE-N and the paramter file of the three replicates are presented
	
#### Migrate-BaleenWhale_Input 

##### 1. Input file
For each species, the input file (.txt) contains:

Line 1. Total number of populations and loci

Line 2. Number of base pairs in the mtDNA sequences

Line 3. Number of sequences for population 1

Line 4-?. MtDNA sequences per sample individual

Line ?. Number of sequences for population 2
	
	
##### 2. Parfile
Parameters employed to for the specific MCMC estimate in MIGRATE-N are included
in the file "parmfile_replicate(A/B/C)". A/B/C represent the three replicates varied only by the random seed .

#### - Migrate-BaleenWhale_Output

Output parameters and skyline output data from MIGRATE-N for each baleen whale species


### - Migrate-Prey_InputOutput

Same information as Folder Migrate-BaleenWhale_InputOutput but for the prey species 
	
### - Correlation

Species_Combined_CSV: This folder includes the skyline output data of the three replicates of whales and prey combined
including the pool mean and pool standard deviation. 
These files were the raw data for the correlation analysis

Temperture_CSV: This folder includes the raw Actic and Antarctic temperature data used for the correlation analysis

Analysis: This folder contains the input files and scripts to run the pearson correlation estimates every 1,000, 2,000, and 5,000 years. 

- Scripts_input correlation

The folder includes the scripts to generate the input files with the pool mean and standard deviatiation in years 
("ExportYear&Ne_fromCombinedCSV_to_CorrelationLR*.R"),
and the scripts to estimate a standard time interval across variables
("Script_GenerateFiles_Approx_*.R")

- Final_results correlations

The folder includes the final input files for the correlation estimate and the script to plot and estimate pearson correlation every 1,000, 2,000, and 5,000 years.


### - Migrate-ComparisonMtgenes_Input

Same information as Folder Migrate-BaleenWhale_Input but for different mtDNA genes and species 
employed for the comparison of temporal trends of different mtDNA genes.


### - Stariway-BaleenWhales_Input

For each of the baleen whale species, the files named "blueprint" are used as both the input and the configuration file for running the "STAIRWAY PLOT v2". The files employed for the plot with minimum coverage of 2x and 10x are included. 

It contains the total number of sites, including the monomorphic sites (line 5) and the folded site frequency spectrum (line 7).
Additional configuration information are also included, like the used mutation rate (line 16) and generation time (line 17).


