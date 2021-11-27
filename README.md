# treedemog
This repository contains code to fit hierarchical Bayesian models of demographic rates (growth, survival, and reproduction) for trees in the eastern US. Models include nonlinear effects of functional traits (wood density, specific leaf area, and maximum height), size (diameter at breast height), mean annual temperature, competition (basal area of neighboring trees), and their interactions, as well as species and plot random effects. 

Demographic data come from the USFS Forest Inventory and Analysis (FIA) program. Trait data come from the TRY plant trait database. Reproductive status data (included in the recruitment model) come from the MASTIF Network. Temperature data are from GridMet. The data files for the growth and survival models are too big for GitHub, so the code is included but can't be run using only the files in this repo (contact me if you'd like the data files). 

The models are written in Stan and fit in R using RStan. The models take one or more days to fit on a good desktop or HPC cluster. The model output files are also too big to fit on GitHub, but I've included RMarkdown files that show model diagnostics, parameter estimates, model checks, etc.

The models describe the effects of traits on demographic rates (i.e., performance landscapes) and how they vary across the temperature gradient using multivariate Gaussian functions. Performance landscapes showing the effects of wood density and maximum height on growth, survival, and recruitment (as well as fitness, estimated using integral projection models) are shown below:


![](results/wd_sla_landscapes.PNG?raw=true)
