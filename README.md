<img align="right" width="170" height="170" src="https://github.com/marcelglueck/BEpipeR/blob/e902703f223bb39e01afaa7ae16f511b60ef39ca/BEpipeR_logo.png">

# BEpipeR: a user-friendly, flexible, and scalable data synthesis pipeline for the Biodiversity Exploratories and other research consortia
[Marcel Glück](https://orcid.org/0000-0002-9027-6750) | [Oliver Bossdorf](https://orcid.org/0000-0001-7504-6511) | [Henri A. Thomassen](https://orcid.org/0000-0002-9403-1291) 

![GitHub Latest Release)](https://img.shields.io/github/v/release/marcelglueck/BEpipeR) 
[![DOI](https://zenodo.org/badge/734299181.svg)](https://zenodo.org/doi/10.5281/zenodo.10683384)


## Resources
- What the pipeline can do for you: [Features and functionalities](https://github.com/marcelglueck/BEpipeR/blob/main/README.md#features-and-functionalities)
- How to set up the pipeline on your system: [Setting-up](https://github.com/marcelglueck/BEpipeR/blob/main/setup_guide.md) 
- How to operate the pipeline: [BEpipeR publication](https://f1000research.com/articles/13-1268/v1)
- Found a bug? [Report a bug](https://github.com/marcelglueck/BEpipeR/issues)

## Motivation
The wealth of (a)biotic environmental data generated in the [Biodiversity
Exploratories](https://www.biodiversity-exploratories.de/en/) (BE) continues to [grow steadily](https://www.bexis.uni-jena.de/ddm/publicsearch/), 
and so does the effort of using the
data available in our statistical frameworks. Unsurprisingly, many BE projects restrict their analyses to a
handful of frequently used data sets and neglect the wealth of information at their fingertips.
Oftentimes, this might be caused by the need for stringent quality control and (pre-)processing
that many data sets still require. However, this approach might often prevent us
from obtaining a holistic understanding of our complex study systems. To remedy this issue,
this project provides a user-friendly, flexible, scalable, reproducible, and easy-to-expand R pipeline that 
permits the streamlined synthesis of experimental plot data generated by the Exploratories.
We are convinced that this framework will benefit many scientists in the Exploratories, as the
data generated may be used as input in many types of environmental association studies. Additionally, 
this pipeline may be readily adapted to process plot-based data generated by other research consortia.

This project is a registered Biodiversity Exploratories synthesis project.

## Features and functionalities
✔️ **Ease of use:** Parse aggregation information hassle-free through csv parameter files.

✔️ **Flexibility:** One pipeline, three modes. Toggle effortlessly between processing forest or grassland data, or a combination thereof.

✔️ **Deployability:** Run this pipeline on your infrastructure effortlessly, thanks to a reproducible environment.

✔️ **Participatory:** Shape the future of this project by providing suggestions or code.

### Processing steps
1. **Pre-processing:** Template creation, plot location harmonization, data correction and subsetting, taxonomic fallbacks, data reshaping, and normalization by variable
2. **Quality control:** Multi-mode outlier detection
3. **Aggregation:** Within and across data sets (metrics: mean, median, standard deviation (SD), median absolute deviation (MAD)); processing of yearly climate aggregates (incl. the removal of weakly-supported data points; metrics: mean, median, SD, MAD, min, and max)
4. **Diversity calculations:** Normalization by repeated rarefaction; calculating alpha diversity indices (species richness, Simpson, Shannon-Wiener, Margalef, Menhinick, ...)
5. **Post-processing:** Data joining, quality control, and variables selection by variance inflation factor (VIF) analyses
6. **Data export and metadata compilation:** Export of composite data sets and VIF-produced subsets; fetching metadata to the variables produced to assist in preparing the data for publication

## Acknowledgements
People/institutions we are indebted to:
- Founders and staff of the [Biodiversity Exploratories](https://www.biodiversity-exploratories.de/en/): For the envisioning, setting-up, and maintenance of the research platform.
- [Copyright Office](https://uni-tuebingen.de/en/facilities/university-library/publishing-research/publishing/copyright-law/), Tübingen University: For assisting in finding a suitable license for this pipeline.
- [Open Access Publishing Fund](https://uni-tuebingen.de/en/facilities/university-library/publishing-research/publishing/open-access-publication-fund/), Tübingen University: For covering publication fees.




