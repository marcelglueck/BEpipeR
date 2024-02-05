# What output does the pipeline produce?

## Rarefaction
For each data set that undergoes rarefaction, three files are exported to the project's 'Output' directory:
- **<data set ID>_rarefaction_curves_subsample_<subsample size>.png:** Rarefaction curves for each plot. Rarefied diversity is visualized by horizontal lines. The vertical line marks the subsample size, which is also part of the file's name.
- **<data set ID>_rarefaction_curve_slopes_subsample_<subsample size>.csv:** As the the x-axis in rarefaction plots can be quasi-logarithmic (i.e. its increments are way larger than the y-axis' increments), interpreting these graphs might be challenging. To facilitate theri
interpretation, this file listst the slop of each rarefaction curve at the subsampling size selected.

