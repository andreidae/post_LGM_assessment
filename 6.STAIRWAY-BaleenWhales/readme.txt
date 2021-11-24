This directory contain the scripts used for the RAD based analyses (“script” directory)
Additionally, it contains the used data (links in the “rad_data” directory), list of individual identifications (“IDs_files” directory) and the input file used to run stairway plot (“blueprint” directory). 

Each script corresponds to one step of the analysis and was used in the following order:
- Stacks process_radtags: process_radtags.sh
After process_radtags the reads were separated by sample and four files were created per sample (sample_xxx.1.fq, sample_xxx.2.fq, sample_xxx.rem.1.fq, sample_xxx.rem.2.fq). Those are the data files available.
When the same sample was sequenced in more than one library the code in “cat_command” was used.
- Bowtie: bowtie2_alig.sh
- Samtools: sam_to_sortedbam.sh
-  Angsd: sfs.sh followed by sfs2.sh
After the site frequency spectrum was created it was added to the corresponding blueprint file. All the blueprint files used are attached. The blueprint files are the input for stairway plot.
-  Stairway plot: at the time stairway plot was run with the following command (available at the manual ver. 2.0 beta): 
java -cp stairway_plot_es Stairbuilder file.blueprint
The command above creates the script: file.blueprint.sh
followed by: file.blueprint.plot.sh
