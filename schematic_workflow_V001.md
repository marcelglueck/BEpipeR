# How to add new data sets to the datasets_summary file?
1. Download the data set and de-compress in the working copy directory of the project. Data stored there will not be used by the pipeline but serves as a go-to location for inspecting the data yourself.
2. Copy the csv data file to the project's source directory. From there, it will be copied to the project's input directory at the start of each pipeline run.
3. Inspect both data and metadata:
   - Data:
     -  Is most conviniently inspected in the office suite of your choice.
     -  Check whether it contains undesired factor levels, improper NA values (e.g. -888888, character values).
     -  Decide for yourself, whether the use of NA values is appropriate or whether NAs might better be replaced with zeros.
     -  Copy the columns of interest to a new row of the data sets summary file. As stressed in the file's dictionary, ensure that plotIDs are provided in column C1 only. If you, by accident include character columns, do not worry. They will automatically be excluded by the pipeline.
    - Metadata:
      - Check the provided metadata and datastructure files carefully. This will inform yor processing approach.
4. Fill out the metadata column in the data sets summary file.
5. Based on the information gathered, decide on how to process the data set and enter this information in the data sets summary file. Again, the provided dictionary is your best friend if you are unsure about how to encode the required information.

**Notes on the helpers for subsetting and data wrangling:**
- The information entered is always processed from top to bottom, meaning that the order of input matters.
- The data wrangling part of the pipeline supports both value and pattern-based approeaches. The pattern-based approach is most suited to remove factor levels based on partial matches (e.g. ...), while the value-based approach performs exact replacements.


6. Ensure that the aggregation information is complete.
7. Export as csv file and place in the Helper directory. If the naming of the file is maintained, there is no need to update its name in the pipeline. If you change its name, change its name in the import function (Line XXX) accordingly.
8. Open the R project. Ensure that the reproducible environment is set up successfully.
9. Execute the header lines. Ensure that there are no errors.
10. If no errors were observed, run the pipeline from there. You will notice that we made the pipeline quite verbose, i.e. the processing progress is printed frequently.
11. If the pipeline has been executed successfully, you might notice that not all lines executed might be visible in the console anymore. To change this behavior, increase the max number of lines visible in the console in RStudio. However, this change only takes effect after you have re-started RStudio. Still, do not worry. You will find all prompts of the pipeline in the console_output.txt file in the project's output directory.
12. Inspect potential graphical output exported to the project's Output directory and decide for yourself whether you call the processing a success.

