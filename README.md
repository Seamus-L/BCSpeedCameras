This project uses python in a difference-in-difference framework to estimate the causal effect of speed cameras on in-intersection collisions in British Columbia, Canada. All work is completed in jupityr notebooks for python. Of note, this project uses a matching framework to construct a suitable control group for the difference-in-difference regression.


For background, details of methodology, and outcomes, see the PDF report that accompanies the file.


Raw data was collected directly from the Insurance Company of British Columbia (ICBC). This is provided at the interesection level. Additional data was collected from ICBC for the location of red light cameras. This can be found at the following sources:

- https://www.icbc.com/about-icbc/newsroom/Statistics
- https://www.icbc.com/road-safety/community/intersection-safety-camera-program


Known issues:
- Matching not generating high propensity scores - could potentially be addressed by adding additional covariates, but only a small sample of treated units
- Adjust matching threshold for consistency with literature (Marco Caliendo & Sabine Kopeinig, 2008)
- Robustness check of alternate matching method (kernel smoothing + kmeans a potential option)
- Additional robustness to restrict smaple to only intersections with red light cameras, as this is the cohort the province was looking at
