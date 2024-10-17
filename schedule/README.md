## Workshop Outline

### Dataset
A trio from the [Genome in a Bottle consortium (GIAB)](https://github.com/genome-in-a-bottle/giab_data_indexes). Time will be required to:
* Download raw data
* Process through the existing workflow FASTQC through to Alignment QC
* Run new workflow components: Variant Calling/Annotation/Prioritization

| Format |  Topic  | Materials | Description |
|:-----------:|:----------:|:--------:|:--------:|
| Lecture | [Workshop Introduction](../lectures/workshop_intro_slides.pdf) | Reuse with some tweaks | A short introduction to the workshop|
| Lecture | [Concepts and considerations for variant analysis in clinical genomics](https://hbctraining.github.io/variant_analysis/lectures/Variant_calling_intro.pdf) | Reuse with replacement of "Cancer / somatic variant calling" section |  |
| Hands-on | [Crash course on Shell basics](https://github.com/hbctraining/BMI713_Intro_to_HPC/blob/master/lessons/01_the_filesystem.md)| Use linked materials | The very basic commands to navigate the filesystem | 
| Lecture | [Introduction to HPC](https://github.com/hbctraining/BMI713_Intro_to_HPC/blob/master/slides/HPC_intro_O2_October2024_BMI713.pdf) | Present lecture / or part of it? | SBATCH, job submission, resources |
| Hands-on | [Project Organization](https://hbctraining.github.io/variant_analysis/lessons/01_data_organization.html) | Reuse with replacement of dataset | Setting up the project space on O2 |
| Hands-on | [Evaluating Read Quality with `FastQC`](https://hbctraining.github.io/variant_analysis/lessons/02_fastqc.html) | Reuse with replacement of dataset | Understanding QC of sequence reads |
| Hands-on | [Sequence Read Alignment](https://hbctraining.github.io/variant_analysis/lessons/03_sequence_alignment_theory.html) | Reuse with replacement of dataset | Alignmnet with bwa, theory and alignment file format |
| Hands-on | [Alignment File Processing ](https://hbctraining.github.io/variant_analysis/lessons/04_alignment_file_processing.html) | Reuse with replacement of dataset | Mark and remove duplicates, sort BAM file |
| Hands-on | [Alignment File Quality Control](https://hbctraining.github.io/variant_analysis/lessons/05_alignment_QC.html) | Reuse with replacement of dataset (merge with Alignment file processing lesson) | Run Picard CollectAlignmentSummaryMetrics |
| Hands-on | [Aggregating QC metrics using MultiQC](https://hbctraining.github.io/variant_analysis/lessons/06_aggregate_multiqc.html) | Reuse with replacement of dataset  | This can be run later and include GATK and Snpeff results as input. (Qualimap; but might only be for WGS but worth mentioning) |
| Hands-on | Variant Calling | New lesson | remove PON / germline resource / MuTect explanation / MuTect code - Add Haplotype caller explanation and code |
| Hands-on | Variant Annotation | New lesson | remove cancer mode, add annotations from ClinVar, OMIM, dbNSFP (contains many predictive scores as well as ExAC/gnomAD population frequencies)  |
| Hands-on | Variant Prioritization| New lesson | add filters for population frequency (rare), score annotations (damaging), ClinVar pathogenicity, prioritize two hits in the same gene (for suspected recessive disease), prioritize variants found in proband but not parents (for suspected de novo disease) |
| Hands-on | [Visualization in IGV](https://hbctraining.github.io/variant_analysis/lessons/12_IGV.html) | Reuse with replacement of datase t | Maybe expand a bit? |
| Demo | PhenoDB| New lesson | Cohort inheritance analysis. It is built off of ANNOVAR and uses the pedigree information that you input |
