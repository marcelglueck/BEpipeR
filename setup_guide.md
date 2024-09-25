# Step by step: Set up the pipeline's reproducible environment

**Please note:** This guide assumes that you are connected to the internet and use [RStudio IDE](https://posit.co/products/open-source/rstudio/).

1. Download the desired pipeline release from [here](https://github.com/marcelglueck/BEpipeR/releases) and unzip the compressed pipeline files.
3. At the root of the pipeline's directory structure, you will find a file named 'renv.lock'. Open it with a text editor (such as Visual Studio Code). At the top of the file, the required R version for running the pipeline is specified. If you do not have this version of R installed, download it from [here](https://cran.r-project.org/) and install; for Windows machines, ensure that a compatible version of [RTools](https://cran.r-project.org/bin/windows/Rtools) is installed as well.
4. Set the required R version as default: In RStudio, go to 'Tools' > 'Global Options ...'. Under 'R Session; R version' click 'Change' and select the required version of R; close RStudio.
4. Open the BEpipeR.Rproj file in RStudio; the package for setting-up the reproducible environment, *renv*, will be bootstrapped automatically. Subsequently, it will prompt that packages recorded in the lockfile are not installed on your system yet.
5. Type ```renv::restore()``` and confirm the prompted dialog with 'y'; *renv* will download and install all packages required to a per-project library.
6. For the visualization of plot locations, the border of Germany must be obtained as gpkg file from [GADM](https://geodata.ucdavis.edu/gadm/gadm4.1/gpkg/gadm41_DEU.gpkg), and stored as 'Germany_borders.gpkg' in the pipeline's 'Helpers' directory. 

For increasing the number of lines retained in RStudio's console to a reasonable number, try `rstudioapi::writeRStudioPreference("console_max_lines", 20000L)` (restart of RStudio required). Unfortunately, this approach might not work for all RStudio releases, which is why you might want to consult the internet for a more suitable approach. 
