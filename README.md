<img align="right" width="170" height="170" src="https://github.com/marcelglueck/BEpipeR/blob/e902703f223bb39e01afaa7ae16f511b60ef39ca/BEpipeR_logo.png">

# BEpipeR: a user-friendly, flexible, and scalable data synthesis pipeline for the Biodiversity Exploratories and other research consortia
[Marcel Glück](https://orcid.org/0000-0002-9027-6750) | [Oliver Bossdorf](https://orcid.org/0000-0001-7504-6511) | [Henri A. Thomassen](https://orcid.org/0000-0002-9403-1291) 

[![Github All Releases](https://img.shields.io/github/downloads/marcelglueck/BEpipeR/total.svg)]() 
![GitHub Latest Release)](https://img.shields.io/github/v/release/marcelglueck/BEpipeR) 
[![DOI](https://zenodo.org/badge/734299181.svg)](https://zenodo.org/doi/10.5281/zenodo.10683384)


## Quick-start
- What the pipeline can do for you: [Features and functionalities](https://github.com/marcelglueck/BEpipeR/blob/main/README.md#features-and-functionalities)
- How to set up the pipeline on your system: [Setting-up](https://github.com/marcelglueck/BEpipeR/blob/main/setup_guide.md) 
- How to operate the pipeline: Publication to BEpipeR v1.0.0 release
- Found a bug? [Report a bug](https://github.com/marcelglueck/BEpipeR/issues)

## Motivation
The wealth of (a)biotic environmental data generated in the [Biodiversity
Exploratories](https://www.biodiversity-exploratories.de/en/) continues to [grow steadily](https://www.bexis.uni-jena.de/ddm/publicsearch/), 
and so does the effort of implementing always the
newest data into our statistical frameworks. Unsurprisingly, many BE projects restrict their analyses to a
handful of frequently used data sets, neglecting the wealth of information at their fingertips.
Oftentimes, this might be caused by the need for stringent quality control and (pre-)processing
that many environmental data sets still require. However, this approach might often prevent us
from obtaining a more complete understanding of our complex study systems. To remedy this issue,
this project provides a comprehensive user-friendly, flexible, scalable, reproducible and easy-to-expand R pipeline that 
permits for the streamlined synthesis of (a)biotic EP-level data generated by the Exploratories.
We are convinced that such a framework will benefit many scientists in the Exploratories, as the
data generated might be used as input in many types of environmental association studies. Additionally, 
with modifications, this pipeline might be readily adapted to process plot-based data generated by other research consortia.

This project is a registered Biodiversity Exploratories synthesis project.

## Features and functionalities
✔️ **Flexibility:** One pipeline, three modes. Switch between forest, grassland, and combined (forest & grassland) mode effortlessly. 

✔️ **Ease of use:** Simply parse aggregation information through csv parameter files.

✔️ **Customizability:** Easily adapt the pipeline to your own needs by e.g. subsetting the template for your plots of interest.

✔️ **Deployability:** Run this pipeline on your infrastructure effortlessly, thanks to a reproducible environment.

✔️ **Participatory:** Shape the future of this project by either providing suggestions or participate by coding.

### Processing performed
1. **Data preparation and wrangling:** Template creation, plot locations harmonization, values correction, subsetting, fallbacks to more basal (taxonomic) levels, data reshaping, normalization by variable (for e.g. sampling effort)
2. **Quality control:** Multi-mode outlier detection
3. **Data aggregation:** Both within and across data sets (mean, median, SD, MAD); processing of yearly climate aggregates (incl. the removal of poorly-supported data points)
4. **Diversity indices:** Normalization by (repeated) rarefaction; calculating species richness, Simpson/Shannon-Wiener/Margalef/Menhinick index, ...
5. **Post-processing:** Data joining, quality control, variables selection by variance inflation factor (VIF) analyses
6. **Data export and metadata compilation:** Export of composite data sets and VIF-produced subsets; fetching metadata to the variables produced to assist in preparing the data for publication, submission to BExIS, etc ...

## Acknowledgements
People/institutions we are indebted to:
- Founders and staff of the [Biodiversity Exploratories](https://www.biodiversity-exploratories.de/en/): For the envisioning, setting up, and maintenance of the research platform.
- [Executive department on German copyright law](https://uni-tuebingen.de/en/facilities/university-library/publishing-research/publishing/copyright-law/), Tübingen University: For assisting in finding a suitable license for this pipeline.
- [Open access publishing fund](https://uni-tuebingen.de/en/facilities/university-library/publishing-research/publishing/open-access-publication-fund/), Tübingen University: For covering publication fees.




