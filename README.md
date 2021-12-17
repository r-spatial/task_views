# Impending change: 

All CRAN Task Views will be handled and published from https://github.com/cran-task-views within weeks rather than months (so early in 2022), so any issues should be raised after migration to markdown has been completed and this repository archived.

# Spatial and SpatioTemporal Task Views

*Local copy for editing the Spatial and SpatioTemporal Task View pages.*

This repo contains the Spatial and SpatioTemporal Task View pages in ctv format from the R-Forge **ctv** package, to enable receipt of PRs from those wishing to help keep them up to date.
Only TV maintainers can sync them with the R-Forge SVN **ctv** repo. 
Any PRs should suggest edits to the files in the ctv folder only.
The ctv markup format is described in <https://cran.r-project.org/web/packages/ctv/vignettes/ctv-howto.pdf>.

Test your changes using the code below before submitting any PR:

```r
library(ctv)
ctv2html(read.ctv("ctv/Spatial.ctv"))
check_ctv_packages("ctv/Spatial.ctv")
```
