This project uses python in a difference-in-difference framework to estimate the causal effect of speed cameras on in-intersection collisions in British Columbia, Canada. All work is completed in jupityr notebooks for python. Of note, this project uses a matching framework to construct a suitable control group for the difference-in-difference regression.

This is a work in progress and will be updated ocassionally.

UPDATE: Recent work has produced a null-result, in contrast with the strongly significant results found initially. Must work later to diagnose whether it is a true negative, or if there are more issues with matching, as the histogram does not reflect a high-quality matching, although, pre-trends are much more parallel now.


For background, details of methodology, and outcomes, see the PDF report that accompanies the file.


Raw data was collected directly from the Insurance Company of British Columbia (ICBC). This is provided at the interesection level. Additional data was collected from ICBC for the location of red light cameras. This can be found at the following sources:

- https://www.icbc.com/about-icbc/newsroom/Statistics
- https://www.icbc.com/road-safety/community/intersection-safety-camera-program



Ongoing work and known issues:
- Matching not generating high propensity scores - plan to address by adding additional covariates
- Adjust matching threshold for consistency with literature (Marco Caliendo & Sabine Kopeinig, 2008)
- Have not plotted matching histogram to verify results of matching
- Robustness check of alternate matching method (kernel smoothing + kmeans a potential option)
- Additional robustness to restrict smaple to only intersections with red light cameras, as this is the cohort the province was looking at
