# Module 08 - Data management templates

Here we present a series of templates and examples to help you get started in managing your data.

## Quick start guide to directory structure

As an emerging biodiversity genomics researcher, the first question you may have when you receive your first batch of genomic data is likely to be: What do I do with this? Your first step should always be to ensure that you keep an untouched backup copy of the raw data in [cold storage](https://genomicsaotearoa.github.io/data-management-resources/modules/module09/). The raw data should be stored alongside all relevant [metadata](https://genomicsaotearoa.github.io/data-management-resources/modules/module04/).

With that done, you next want to move the data to your analysis space, and set up your directory structure. Having clearly structured directories keeps things tidy, and ensures that you can always tell where you are up to in your analysis pipeline. It is very likely that the first thing you want to check will be the quality of your raw data, so let’s set up a directory structure that will hold our raw data and do some quality control steps.

```
.
|--- first-sequencing-project/
|	|--- raw-data/
|		|--- 2023-01-30-sequencing.fastq.gz
|	|--- scripts/
|		|--- 01-fastqc.sh
|	|--- outputs/ 
|		|--- 01-fastqc/
```

Here you can see the top level directory `first-sequencing-project` will contain everything to do with this project all in one place. Within this project directory there are three subdirectories: `raw-data`, `scripts`, and `outputs`. By using simple, clear naming, the directory structure should be self-explanatory. 

Our raw data, in the form of a compressed FASTQ file, is held in the `raw-data/` directory. Scripts for processing the data, like the  bash script `01-fastqc.sh` for running FastQC are all kept in one place. Using a numbering system for scripts and their associated output directories (like the `01-fastqc/` subdirectory within the `outputs/` directory) is helpful to keep track of the steps in the analysis pipeline.

The script to run FastQC to check sequencing quality should direct outputs to the `./first-sequencing-project/outputs/01-fastqc/` directory. Once we run this analysis, we will find the output FastQC results files there.

From here, it’s easy to see how you can build up your analysis pipeline from the `scripts/` directory, creating new numbered subdirectories in `outputs/` for each associated set of output files produced.
