# Step-by-step: Setting up the pipeline's reproducible environment

**Important:** Do not modify the files/directories provided. This might break the pipeline. If you think you might have modified them unintentionally, download the pipeline files anew.

1. Download the desired pipeline release from [here](https://github.com/marcelglueck/BEpipeR/releases).
2. Unzip the downloaded and compressed pipeline files.
3. Open the provided renv.lock file. If you do not see it, configure your operating system to display hidden files.
4. At the very top of the file, the required R version is specified.
If you do not have the required version of R installed ...
   1.  Download the required version from [here](https://cran.r-project.org/).
   2.  In RStudio, go to 'Tools" > 'Global Options ...'. Under 'R Session; R version' click 'Change' and select the required version of R
   3.  Restart RStudio
   
6. Open the Rproject file (it should open in RStudio); the package for the reproducible environment is downloaded automatically
7. Following its download, renv will prompt that packages recorded in the lockfile are not installed on your system yet.
8. Type ```renv::restore()```; confirm the prompted dialog with "y".
9. renv will download and install all required packages.
10. After all packages have been restored successfully, you are ready to go 🥳
