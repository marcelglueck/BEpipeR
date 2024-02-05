# What output does the pipeline produce?

## Rarefaction
For each data set that undergoes rarefaction, three files are exported to the project's 'Output' directory:
- **<data set ID>_rarefaction_curves_subsample_<subsample_size>.png:** Rarefaction curves for each plot. Rarefied diversity is visualized by horizontal lines. The vertical line marks the subsample size, which is also featured in the file's name.
- **<data set ID>_rarefaction_curve_slopes_subsample_<subsample size>.csv:** As the the x-axis in rarefaction plots can be quasi-logarithmic (i.e. its increments are way larger than the y-axis' increments), interpreting these graphs might be challenging. To facilitate their interpretation, this file lists the slope of each rarefaction curve at the subsampling size selected.
- <data set ID>_rarefaction_curve_slopes_subsample_<subsample size>.png: A graphical representation of the information stored in <data set ID>_rarefaction_curve_slopes_subsample_<subsample size>.csv.

# Final quality control
- **FQC_env_var_composite_complete:** The quality-controlled composite, after excluding columns that have non-numeric content, are mono-value or feature NA/NaN/Inf. No variables selection was performed on this ouput. Use this file if you would like to perform variables selection yourself or subset it for the variables you are most interested in.

## Variables selection
- VS_VIF<VIF_threshold>_VS_analysed_vars: All variables used in variables selection.
- VS_VIF<VIF_threshold>_VS_retained_vars_scores.csv: Variables retained and their VIF score after excluding cross-correlated variables by a stepwise variance inflation factor analysis with VIF_threshold. 
- VS_VIF<VIF_threshold>_VS_composite.csv: FQC_env_var_composite_complete after excluding all variables deemed cross-correlated (i.e. only the variables lsited in VS_VIF<VIF_threshold>_VS_retained_vars_scores.csv are listed here)
- VS_VIF<VIF_threshold>_VS_corr_matrix.csv: Pairwise Pearson's r for all variables retained at <VIF_threshold>. This might facilitate downstream model interpretation.
- VS_VIF<VIF_threshold>_VS_excluded_vars.csv: Variables that have been excluded at <VIF_threshold>. 
