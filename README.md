<img align="right" width="190" height="190" src="https://github.com/marcelglueck/BEpipeR/blob/e902703f223bb39e01afaa7ae16f511b60ef39ca/BEpipeR_logo.png">

# BEpipeR: a user-friendly, flexible, scalable, and easily expanded pipeline for a streamlined processing of biotic and abiotic data in R  
[![Github All Releases](https://img.shields.io/github/downloads/marcelglueck/BEpipeR/total.svg)]()
![GitHub Latest Release)](https://img.shields.io/github/v/release/marcelglueck/BEpipeR)
[![DOI](https://zenodo.org/badge/734299181.svg)](https://zenodo.org/doi/10.5281/zenodo.10683384)

## People involved
- [Marcel Glück](https://orcid.org/0000-0002-9027-6750) (PI, conceptualization, coding, implementation, maintenance, documentation)
- [Henri Thomassen](https://orcid.org/0000-0002-9403-1291) (conzeptualization)
- [Oliver Bossdorf](https://orcid.org/0000-0001-7504-6511) (conzeptualization)

**You are interested in joining? Get in touch with us!**

## Updates
### 20.02.2024
- **BEpipeR v0.1.0 has been released!** 🥳 This release is already meant for productive purposes (i.e. it is fully functional with regards to forest plot data). We will fully implement support for grassland plots very soon. That release will also allow you to toggle between forest and grassland mode easily.

## Background and motivation
The wealth of biotic and abiotic environmental data generated in the [Biodiversity
Exploratories](https://www.biodiversity-exploratories.de/en/) continues to [grow steadily](https://www.bexis.uni-jena.de/ddm/publicsearch/), and so does the effort of implementing always the
newest data into our statistical frameworks. Unsurprisingly, many BE projects restrict their analyses to a
handful of frequently used data sets, neglecting the wealth of information at their fingertips.
Oftentimes, this might be caused by the need for stringent quality control and (pre-)processing
that many environmental data sets still require. However, this restraint might often prevent us
from obtaining a more complete understanding of our complex study systems. Hence, the aim
of this project is to establish a user-friendly, flexible, scalable, and easy-to-expand R
framework that permits the processing of (a)biotic data generated by the Exploratories.
We believe that such a framework will also benefit other scientists in the Exploratories, 
as the generated data can be used as input in any type of environmental association study.

This project is a registered BE synthesis project.

## The pipeline's main features
- **Easy to use**: Simply parse the required aggregation information through the provided parameters files. No coding required.
- **Flexibility:** Biological data comes in many different shapes. We tried to accommodate them all. If you feel that you cannot aggregate your data with the approaches available, please get in touch with us.
- **Easy to deploy**: You will be able to deploy this pipeline on many systems without modifications, as this pipeline adheres to best practice approaches on reproducibility and interoperability.
- **Easy to debug and feature-expand**: Compressed code, the processing through a few major
loops, and consistent variables naming facilitate debugging and future feature implementations. In particular in the light of current high-paced discussions about good practice in data processing (e.g. [1](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003531) and [2](https://journals.asm.org/doi/full/10.1128/msphere.00355-23)), a flexible framework that can accommodate novel insights with little effort is more than timely.
- **Transparent and tractable**: The main parameters file is updated on-the-fly to reflect the current state of processing, allowing the user to monitor the pipeline’s progress. Also, all derived variables in the composite data sets produced  feature data set IDs. So, you will always be able to track information back to their original data sets.

## What does the current version of the pipeline do?
1. **Data preparation and wrangling:** Template creation, plot locations harmonization, correction of suspicious (NA) values, sub-setting, fallbacks to more basal (taxonomic) levels, data reshaping, normalization by variable (for e.g. sampling effort)
2. **Quality control:** Multi-mode flagging and removal of putative erroneous values
3. **Data aggregation:** Both within and across data sets (mean, median, SD, MAD); processing of yearly climate aggregates (incl. the removal of poorly-supported data points)
4. **Diversity indices:** Normalization by repeated rarefaction; calculating species richness, Simpson/Shannon-Wiener/Margalef/Menhinick index, ...)
5. **Post-processing:** Data joining, quality control, variables selection by variance inflation factor (VIF) analyses with thresholds from two to ten
6. **Data export and metadata compilation:** Export of the whole data composite and all VIF-produced subsets; fetching metadata to the variables produced to assist in preparing the data for publication, submission to Bexis, etc ...

## FAQ
### What to do if you find an undesired behaviour/bug in the pipeline?
First, please make sure that the potential issue you found is valid by inspecting the data produced by this section of the code carefully. If, after thorough inspection, you are still sure that you found an issue warranting correction, please bring this as soon as possible to the attention of [Marcel Glück](https://orcid.org/0000-0002-9027-6750) using the [bug report template](issues_template.txt).
### What to do if you find suspicious values in the data?
First, please ensure that the suspicious value found is not a false positive. The pipeline assists in finding and excluding suspicious values fairly extensively. Accordingly low should be their prevalence in the final data sets. If, after checking, you are still sure that you found such a value, please bring this to the attention of Marcel Glück as soon as possible using the [bug report template](issues_template.txt). For erroneous information in metadata, an informal email to MG suffices.
### How to set up the pipeline on my system?
This pipeline uses the [renv package](https://rstudio.github.io/renv/articles/renv.html) to restore a reproducible environment we have set up. This means that the package installs all packages needed for an issue-free execution of the pipeline (i.e. the ones that were used to code this pipeline in the first place). For a step-by-step guide, please see [here](setup_guide.md). Installing all required packages like this is highly recommended and we will not try to troubleshoot potential issues caused by installing the required packages manually.
### Where can I find the manual?
We do not provide a comprehensive manual yet. However, very soon, we will submit a large composite data set with 950+ variables to Bexis. As metadata, we will include the data sets summary file that will allow you to fully reproduce the processing. This file is also meant to be a go-to example on how to encode aggregation information through the summary file. This in combination with the file's dictionary should allow you to understand the encoding pretty intuitively. Also, in the script, we provide comments on the reasoning and each step performed throughout. If you want to adopt this framework for your own purposes by adding data sets, see this brief [schematic workflow](https://github.com/marcelglueck/BEpipeR/blob/main/BEpipeR_workflow.svg). You also might appreciate this [explanation](output_description.md) of the output produced by this pipeline.
### Can I already use this pipeline to process grassland data without any modifications?
Unfortunately, not yet, but this feature will be implemented swiftly after the initial release of the pipeline. In the meantime, you can already start inspecting the grassland data sets you would like to include and enter this information in the data sets summary file. After we have implemented this feature, you will be able to toggle between grassland and forest mode easily.
### I want to use this pipeline for aggregating quite some data sets from the Biodiversity Exploratories. What do I need to consider?
Keep in mind that if you are interested in working on data sets from more than three projects, you will need to have a synthesis proposal. But do not panic! The corresponding Word template is only one page long and your proposal does not undergo a formal approval process. Just state what the additional benefits of aggregating multiple data sets might be. You can find the template in Bexis.
### How do I attribute this pipeline?

**Please cite this pipeline as (replace the X.X.X with the actual pipeline version used):**

Glück M., H. A. Thomassen and O. Bossdorf (2024). BEpipeR: a user-friendly, flexible, scalable, and easily expanded pipeline for a streamlined processing of biotic and abiotic data in R. vX.X.X. Zenodo. https://zenodo.org/doi/10.5281/zenodo.10683384

Please do so if you use the pipeline or parts of it in your own work. If you use data produced through this pipeline, please cite both the data set and this pipeline. If you share the code with someone else, please share the whole project, as separating any project file from the license file is not permitted. For more information, see the pipeline's license file. 

### What does the workflow look like?
The pipeline makes a very complex tasks as easy as possible. It boils down to answering a few questions about your data set. Here is an excerpt of full workflow that can be obtained from [here](https://github.com/marcelglueck/BEpipeR/blob/main/BEpipeR_workflow.svg) as vector graphic.



## Acknowledgements
People and/or institutions we are indebted to:
- [Executive department on German Copyright Law](https://uni-tuebingen.de/en/facilities/university-library/publishing-research/publishing/copyright-law/), Tübingen University: For assisting in finding a suitable license for this pipeline.



