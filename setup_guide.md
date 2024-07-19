# Step by step: Set up the pipeline's reproducible environment

**Important:** Do not modify the files/directories provided, as this might break the pipeline. If you think you might have modified them unintentionally, download the pipeline anew. This guide assumes that you are connected to the internet and use [RStudio IDE](https://posit.co/products/open-source/rstudio/).

1. Download the desired pipeline release from [here](https://github.com/marcelglueck/BEpipeR/releases).
2. Unzip the BEpipeR_vX.X.X.zip file.
3. At the root of the pipeline's directory structure, you will find a file named renv.lock. Open it with a text editor (such as Visual Studio Code). At the top of the file, the required R version for running the pipeline is specified. If you do not have this version of R installed, download the required version from [here](https://cran.r-project.org/) and install; for Windows machines, ensure that a compatible version of [RTools](https://cran.r-project.org/bin/windows/Rtools) is installed as well
4. Set the required R version as default: In RStudio, go to 'Tools' > 'Global Options ...'. Under 'R Session; R version' click 'Change' and select the required version of R; close RStudio
4. Open the BEpipeR.Rproj file in RStudio; the package for setting-up the reproducible environment will be bootstrapped automatically. Subsequently, it will prompt that packages recorded in the lockfile are not installed on your system yet.
5. Type ```renv::restore()``` and confirm the prompted dialog with 'y'; renv will download and install all packages required to a per-project library.
6. For the visualization of plot locations, the borders of Germany must be obtained as gpkg file from [GADM](https://geodata.ucdavis.edu/gadm/gadm4.1/gpkg/gadm41_DEU.gpkg), and stored as 'Germany_borders.gpkg' in the pipeline's 'Helpers' directory. 
