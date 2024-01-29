# ITP_AMSPAPS_23-24_spectralraoq
Spectral Rao's Q Biodiversity Index computing using SPOT multispectral satellite images with Python language

This repository provides a main code for SPOT satellite images treatment, with the objective to compute the spectral Rao's Q
index of biodiversity, that allows to make a discret analysis of data. The input files are satellite images with RGB bands 
and NIR by using SPOT keys protocols (https://earth.esa.int/eogateway/documents/20142/37627/SPOT-6-7-imagery-user-guide.pdf).
The calculation is based on the Spectral Variation theory by using NDVI as index. The input parameters of the code are 
"NVDI_Mask", "Window_Size" and "NaN_Tolerance". Where, "NVDI_Mask" is the threshold that differenciates the non-forest 
surfaces (NVDI_Mask = 0.80 by default); "Window_Size" corresponds to the windows size, related with the targeted ground surface
size analysis of biodiversity, for example, in SPOT 7 case, with 1.5 meters of resolution, we use a 9x9 pixel size window, that
represents a 182.25 squared meters windows pixel biodiversity analysis (Window_Size = 9 by default); "NaN_Tolerance" represents 
the number of NaN pixels values tolerated on the one-by-one-window computing process.

The products are GEOJason files with RGB, NDVI and Rao's index georreferentiated information for further analysis.

There is assumed that other masks preprocessing where already considered in .TIF files production, as cloud mask, canopy shadow,
etc.

Updated January 29th, 2024.
