<img align="right" width="170" height="170" src="https://github.com/marcelglueck/BEpipeR/blob/e902703f223bb39e01afaa7ae16f511b60ef39ca/BEpipeR_logo.png">

# BEpipeR: a user-friendly, flexible, scalable, and easily expanded pipeline for a streamlined processing of biotic and abiotic Biodiversity Exploratories data in R  
[Marcel Glück](https://orcid.org/0000-0002-9027-6750) | [Henri Thomassen](https://orcid.org/0000-0002-9403-1291) | [Oliver Bossdorf](https://orcid.org/0000-0001-7504-6511)

[![Github All Releases](https://img.shields.io/github/downloads/marcelglueck/BEpipeR/total.svg)]() 
![GitHub Latest Release)](https://img.shields.io/github/v/release/marcelglueck/BEpipeR) 
[![DOI](https://zenodo.org/badge/734299181.svg)](https://zenodo.org/doi/10.5281/zenodo.10683384)


## Quick-start
- What the pipeline can/cannot do for you: [Features and limitations](https://github.com/marcelglueck/BEpipeR?tab=readme-ov-file#what-does-the-current-version-of-the-pipeline-do)
- How to set up the pipeline on your system: [Setting-up](https://github.com/marcelglueck/BEpipeR/blob/main/setup_guide.md) 
- How to operate the pipeline and parse processing information: [Parsing processing information](https://github.com/marcelglueck/BEpipeR/blob/main/BEpipeR_workflow.svg)
- Found a bug? [Report a bug](https://github.com/marcelglueck/BEpipeR/issues)

## Motivation
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

## What does the current version of the pipeline do?
1. **Data preparation and wrangling:** Template creation, plot locations harmonization, correction of suspicious (NA) values, sub-setting, fallbacks to more basal (taxonomic) levels, data reshaping, normalization by variable (for e.g. sampling effort)
2. **Quality control:** Multi-mode flagging and removal of putative erroneous values
3. **Data aggregation:** Both within and across data sets (mean, median, SD, MAD); processing of yearly climate aggregates (incl. the removal of poorly-supported data points)
4. **Diversity indices:** Normalization by repeated rarefaction; calculating species richness, Simpson/Shannon-Wiener/Margalef/Menhinick index, ...)
5. **Post-processing:** Data joining, quality control, variables selection by variance inflation factor (VIF) analyses with thresholds from two to ten
6. **Data export and metadata compilation:** Export of the whole data composite and all VIF-produced subsets; fetching metadata to the variables produced to assist in preparing the data for publication, submission to Bexis, etc ...

## The pipeline's main features
- **Easy to use**: Simply parse the required aggregation information through the provided parameters files. No coding required.
- **Flexibility:** Biological data comes in many different shapes. We tried to accommodate them all. If you feel that you cannot aggregate your data with the approaches available, please get in touch with us.
- **Easy to deploy**: You will be able to deploy this pipeline on many systems without modifications, as this pipeline adheres to best practice approaches on reproducibility and interoperability.
- **Easy to debug and feature-expand**: Compressed code, the processing through a few major
loops, and consistent variables naming facilitate debugging and future feature implementations. In particular in the light of current high-paced discussions about good practice in data processing (e.g. [1](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003531) and [2](https://journals.asm.org/doi/full/10.1128/msphere.00355-23)), a flexible framework that can accommodate novel insights with little effort is more than timely.
- **Transparent and tractable**: The main parameters file is updated on-the-fly to reflect the current state of processing, allowing the user to monitor the pipeline’s progress. Also, all derived variables in the composite data sets produced  feature data set IDs. So, you will always be able to track information back to their original data sets.

## FAQ
### How do I attribute this pipeline?
**Please cite this pipeline as (replace the X.X.X with the actual pipeline version used):**

Glück M., H. A. Thomassen and O. Bossdorf (2024). BEpipeR: a user-friendly, flexible, scalable, and easily expanded pipeline for a streamlined processing of biotic and abiotic data in R. vX.X.X. Zenodo. https://zenodo.org/doi/10.5281/zenodo.10683384

Please do so if you use the pipeline or parts of it in your own work. If you use data produced through this pipeline, please cite both the data set and this pipeline.

## Acknowledgements
People and/or institutions we are indebted to:
- [Executive department on German Copyright Law](https://uni-tuebingen.de/en/facilities/university-library/publishing-research/publishing/copyright-law/), Tübingen University: For assisting in finding a suitable license for this pipeline.



