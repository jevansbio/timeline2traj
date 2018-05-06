# timeline2traj
Convert google timeline KMLs to adehabitatLT ltraj objects

Usage in R using the tidykml package:

```R
devtools::install_github("briatte/tidykml")
library(tidykml)
setwd("C:/Users/Julian/Downloads/timeline")
#read in all days kml files
allpoints=do.call(rbind,lapply(dir(),function(x) kml_points(x)))

traj=kml2traj(allpoints)


