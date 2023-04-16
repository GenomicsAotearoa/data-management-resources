# Module 08 - Incorporating data management into daily practice

<img src="https://github.com/GenomicsAotearoa/data-management-resources/blob/main/docs/figures/under-construction_geek_man_01.png?raw=true" alt="Under Construction sign" style="height:300px;">

This page is currently under construction. Come back later.


Knowing where to start can be one of the hardest parts of the data management journey, but getting good practices in place early will save you from headaches down the track. There is a wealth of existing information on these and other important concepts for the research lifecycle, with this Module acting as a 'quick start' guide, giving a brief overview of important considerations such as directory structure and file naming conventions, the use of version control, and workflow management. 

Beyond this Module, we recommend you investigate your institute's resources, as they may provide specific guidelines that meet institutional criteria. [The Carpentries](https://carpentries.org/) provide workshops and extensive documentation across a wide range of subject areas that can help you get started. We also recommend you familiarise yourself with the fundamental principles of tidy data as soon as possible in your research journey. 

Whatever your approach, we recommend consistency above all else. Maintaining comprehensive and consistent notes across all aspects of the research, from proposed research questions, existing scholarship, involvement of collaborators, data collection and generation procedures, and analysis (regardless of whether it was successful) will not only ensure reproducibility, but make your research papers faster and easier to write!  

## Data management fundamentals
 
As an emerging biodiversity genomics researcher, the initial question you will have when you receive your first batch of genomic data is likely to be: *What do I do with this?* Your first step should always be to ensure that you keep an untouched backup copy of the raw data in [cold storage](https://genomicsaotearoa.github.io/data-management-resources/modules/module03/). All relevant [metadata](https://genomicsaotearoa.github.io/data-management-resources/modules/module07/) should be stored alongside the raw data (for example, in README files.


!!! info "Validating data transfer"
    
    Whenever you transfer data, you will want to validate it, to ensure that the transfer completed with no errors and the files are intact. [Checksums](https://www.archives.govt.nz/manage-information/how-to-manage-your-information/digital/checksums/the-importance-of-checksums) are a key validation tool. A checksum for a given file will always be the same no matter where the file is.

    !!! terminal "script"

        To generate a checksum for a the raw file in your local directory:

        ```bash
          md5sum raw-data.fastq.gz > raw-data.md5
        ```

        !!! quote ""
          On Mac, you will use the `md5` command rather than `md5sum`.
          ```bash
          md5 raw-data.fastq.gz > raw-data.md5
          ```

        To generate checksums for multiple FASTQ files:

        ```bash
          md5sum ./*.fastq.gz > md5sums.txt
        ```

        The output text file will contain a list of the checksums for each of the compressed FASTQ files in the directory.

        !!! quote ""

          The checksum file produced will look something like this:

          ```bash
            c6779ec2960296ed9a04f08d67f64422 ./raw-data-1.fastq.gz
            002c33835b3921d92d8074f3b392ef65 ./raw-data-2.fastq.gz
          ```

        Then to validate the transferred file, copy the output checksum file to the transferred location, and then perform the check:

        ```bash
          cp ./md5sums.txt /final-destination/
          md5sum -c file.md5
        ```

      Each validated checksum will display `OK`, while a mismatched checksum will display `FAILED`. If you get a `FAILED` file, you will need to redo the file transfer and re-validate.


### Directory structure

With that done, you next want to move the data to your analysis space, and set up your directory (folder) structure. Having clearly structured directories keeps things tidy, and ensures that you can always tell where you are up to in your analysis pipeline. It is very likely that the first thing you want to check will be the quality of your raw data, so here we present an example directory structure suitable for that.

  ```bash
    .
    |--- first-sequencing-project/
    |	|--- raw-data/
    |		|--- 2023-01-30-sequencing.fastq.gz
    |	|--- scripts/
    |		|--- 01-fastqc.sh
    |	|--- outputs/ 
    |		|--- 01-fastqc/
  ```

Here you can see the top level directory `first-sequencing-project/` will contain everything to do with this project all in one place. Within this project directory there are three subdirectories: `raw-data/`, `scripts/`, and `outputs/`. By using simple, clear naming, the directory structure should be self-explanatory. 

Our raw data, in the form of a compressed FASTQ file, sits in the `raw-data/` directory. Scripts for processing the data, like the `01-fastqc.sh` bash script are all kept in one place. Using a numbering system for scripts and their associated output directories (like the `01-fastqc/` subdirectory within the `outputs/` directory) is helpful to keep track of the steps in the analysis pipeline.

The `01-fastqc.sh` script that will be used to run FastQC to check sequencing quality should direct outputs to the `./first-sequencing-project/outputs/01-fastqc/` directory. Once we run this analysis, we will put the output FastQC results files there.

From here, it will be relatively straightforward to build up an analysis pipeline from the `scripts/` directory, creating additional numbered subdirectories in `outputs/` for each associated set of output files produced. 
