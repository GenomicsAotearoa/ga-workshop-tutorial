Previous step: [Adding Content](../1.AddingContent)

## Content creation example


### Background

In this section we are going to step through the process of creating a short piece of workshop content, where we have attendees:

 - create a directory structure for their analysis
 - download a small genomic data set
 - run a command to process this data 

Having a simple (preferably well-commented) shell script which carries out the required commands is a good starting point to build a workshop component around.

The following script provides an example:

```
!/bin/sh

# Create directory in which to perform analysis, and change to that directory
mkdir YeastAnalysis
cd YeastAnalysis

# Create subdirectories to hold data and output from FASTQC
mkdir fastq
mkdir fastqc_output

# Change to data directory, and download data from FigShare
cd fastq
wget -O yeast.fastq https://ndownloader.figshare.com/files/4790242

# Run fastqc command on the file yeast.fastq and save the output in fastqc_output
fastqc -o ../fastqc_output yeast.fastq
```

### Setting the scene

Before we get into the details of the workshop content, it is good to provide an overview of what is going to be covered in the session, including specific Learning Objectives for each section of the course.

For the simple exercise we are doing here, the markdown text might be:

```
### Overview

In this section, we will download a small data file containing sequence data from yeast, and then use the `fastqc` command to assess the quality of the data.

#### Learning Objectives

By the end of this section of the course you will have learned:

 1. How to set up your directory structure for your analysis project
 2. How to download the sequencing data (in fastq format) from FigShare
 3. How to run the `fastqc` command (via the command line) and direct the output to a specific directory.
```


### Generating content

Basically we want to take the script, break it into discrete steps, and then write some commentary around each part that explains what the commands are doing, and also provides some rationale for the approach being taken.

### Breaking the script up:

 - Part 1: set up directory structure

    ```
    # Create directory in which to perform analysis, and change to that directory
    mkdir YeastAnalysis
    cd YeastAnalysis

    # Create subdirectories to hold data and output from FASTQC
    mkdir fastq
    mkdir fastqc_output
    ```

- Part 2: download the data

    ```
    # Change to data directory, and download data from FigShare
    cd fastq
    wget -O yeast.fastq https://ndownloader.figshare.com/files/4790242
    ```

- Part 3: run the `fastqc` command

    ```
    # Run fastqc command on the file yeast.fastq and save the output in fastqc_output
    fastqc -o ../fastqc_output yeast.fastq
    ```


### Adding commentary

In between commands we want to have a commentary that explains what is being done and why. This helps the leaners understand the context for what they are learning. It might be descriptions or it might involve the next part of a story that is being told as part of a wider narrative.


For this exercise, the markdown might be:
````
## Set up the directory structure

In order to have a tidy project structure, we want to create directories that will contain the different stages of our analysis. 

```
# Create directory in which to perform analysis, and change to that directory
mkdir YeastAnalysis
cd YeastAnalysis

# Create subdirectories to hold data and output from FASTQC
mkdir fastq
mkdir fastqc_output
```
````


Next step: [Example Content](../3.ExampleContent)
