# Step-by-step: Setting up the pipeline's reproducible environment

**Important:** Do not modify the files provided. If you think you might have modified them unintentionally, download the pipeline files anew.

1. Download the desired pipeline release from [here](https://github.com/marcelglueck/BEpipeR/releases).
2. Unzip the downloaded and compressed pipeline files.
3. Open the provided renv.lock file. If you do not see it, set up your operating system in a way that displays hidden file.
4. At the very top of the file, the required R version is specified.
If you do not have the required version of R installed ...
   1.  Download the required version from [here](https://cran.r-project.org/).
   2.  In RStudion, go 'Tools" > 'Global Options ...'. Under 'R Session; R version' click 'Change' and select the required version of R
   3.  Restart RStudio
   
6. Open the Rproject file (it should open in RStudio).
7. Ignore the warning printed.
8. In the files pane in RStudio, locate the activate.R file; open it.
9. Execute the function diplayed. If not available on your system, the renv package will be downloaded and installed.
10. Following its download, it will prompt that packages recorded in the lockfile are not installed on your system.
11. Type ```renv::restore()```; confirm the prompted dialog with "y".
12. Renv will download and install all required packages.
13. If restoring all packages was successful, you are ready to go 🥳
