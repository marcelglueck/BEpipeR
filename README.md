<img align="right" width="200" height="200" src="https://github.com/marcelglueck/BEpipeR/blob/main/BEpipeR_logo_V003.png">

# BEpipeR: a user-friendly, flexible, scalable, and easily expanded pipeline for a streamlined processing of biotic and abiotic data in R  

## People involved
- [Marcel Glück](https://orcid.org/0000-0002-9027-6750) (PI, conceptualization, coding, implementation, maintenance)
- [Henri Thomassen](https://orcid.org/0000-0002-9403-1291) (conzeptualization)
- [Oliver Bossdorf](https://orcid.org/0000-0001-7504-6511) (conzeptualization)

## Updates
If you are interested in up-to-date news, you have come to the right place. Here we will
inform you about changes to the pipeline incl. future plans, newly-implemented features, 
and bugs/issues found and how to mitigate them.

## Background and motivation
The wealth of biotic and abiotic environmental data generated in the [Biodiversity
Exploratories](https://www.biodiversity-exploratories.de/en/) continues to [grow steadily](https://www.bexis.uni-jena.de/), and so does the effort of implementing always the
newest data into our statistical frameworks. Many BE projects restrict their analyses to a
handful of frequently used data sets, neglecting the wealth of information at their fingertips.
Oftentimes, this might be caused by the need for stringent quality control and (pre-)processing
that many environmental data sets still require. However, this restraint might often prevent us
from obtaining a more complete understanding of our complex study systems. Hence, the aim
of this project is to establish a user-friendly, flexible, scalable, and easy-to-expand R
framework that permits the processing of environmental data generated by the Exploratories.
We believe that such a framework will also benefit other scientists in the Exploratories, 
as the generated data can be used as input in any type of environmental association study.

This project is a registered BE synthesis project.

## Reasons to use the data generated by this pipeline
- **Save time**: No need to process the data sets yourself. Dive right into you analyses.
- **Harness potential**: Why restricting your analyses to a few often-used data sets when you could do better in unravelling complex patterns?
- **Flexibility**: You prefer subsetting for focal variables yourself? Great! Just use the quality-controlled complete composite and perform variable selection to your liking.
- **Improved participation:** By using one of the data sets produced here, you help to make the hard work of many BE scientists visible.

## The pipeline's main features
- **Easy to use**: All important parameters are parsed through xlsx/csv parameters files.
No coding required.
- **Easy to expand**: If adhered to the input format of the parameters files, any type of
environmental information can be pre-processed, aggregated and post-processed
without writing a single line of code.
- **Easy to deploy**: The pipeline can be deployed on many systems without modifications
due to adhering to best practice approaches on reproducibility and interoperability.
- **Easy to debug and feature-expand**: Dense code and the processing through a few major
loops facilitate debugging and future feature implementations.
- **Flexibility**: Regardless of whether you are interested in the complete data set, or
subsets produced by variance inflation factor analyses, we have you covered.
- **Speed**: Time-consuming steps are multi-threaded, reducing processing times.
- **Transparent and tractable**: The main parameters file is updated on-the-fly to reflect
the current state of processing, allowing the user to monitor the pipeline’s progress.
Also, column headers feature dataset IDs to allow users to select environmental
variables by their origin.

## What does the current version of the pipeline do?
1. **Data preparation and wrangling:** Template creation, plot locations harmonization, correction of suspicious (NA) values, sub-setting, fallbacks to more basal (taxonomic) levels, data reshaping, normalization by variable (for e.g. sampling effort)
2. **Quality control:** Multi-mode flagging and removal of putative erroneous values
3. **Data aggregation:** Both within and across data sets (mean, median, SD, MAD); processing of yearly climate aggregates (incl. the removal of poorly-supported data points)
4. **Diversity indices:** Normalization by repeated rarefaction; calculating species richness, Simpson/Shannon-Wiener/Margalef/Menhinick index, ...)
5. **Post-processing:** Data joining, quality control, variables selection by variance inflation factor (VIF) analyses with thresholds from two to ten
6. **Data export and metadata compilation:** Exporting whole composite and all VIF-produced subsets; fetching metadata to the variables produced

## FAQ
### What to do if you find suspicious values in the data?
First, please ensure that the suspicious value found is not a false positive. The pipeline assists in finding and excluding suspicious values fairly extensively. Accordingly low should be their prevalence in the final data sets. If, after checking, you are still sure that you found such a value, please bring this to attention of [Marcel Glück](https://orcid.org/0000-0002-9027-6750) as soon as possible.
### When will the pipeline be released to BE members?
We do not know yet. Currently, we are investigating possible licenses to prevent its un-attributed use. If progress is made in this regard, you will be informed on this page's 'Update' section and through the BE-intern mailing list.

## Technical notes
### Why rarefaction is used for normalization
TBD

## Helpers
You would like to dive deeper into the composite data set. Nice! Here a few functions that 
might come in handy.


### Subsetting for certain data sets or years
```
# Dummy code
test <- "Hello world"
```




