# topocorr
Scripts to apply topographic corrections to data arrays of satellite images. Currently applicable to the C-correction (Teillet et al, 1982) and SCS+C (Soenen et al, 2005). Requires elevation data as input since the C-correction and SCS+C are empirical methods. Easily extendable to other formulas accounting for surface roughness (Minnaert, etc).

Made for use with xarray objects. The input data is generally a dataArray of coordinates (y, x), which can include bands and time dimensions if processing time series of multispectral optical satellite data (Landsat, Sentinel-2, etc). The current script was written for Landsat data processing and relies on the presence of scene-wide metadata on solar azimuth and elevation angles.

The input slope and aspect data must have the same exact griddind, resolution and coordinate system as the optical data to be corrected.

Script coded as one step of a larger project on mapping of soil erosion risk with a long time series of Landsat data.

## References
S. A. Soenen, D. R. Peddle and C. A. Coburn, "SCS+C: a modified Sun-canopy-sensor topographic correction in forested terrain," in IEEE Transactions on Geoscience and Remote Sensing, vol. 43, no. 9, pp. 2148-2159, Sept. 2005, doi: 10.1109/TGRS.2005.852480.

Teillet, P. M., Guindon, B. and Goodenough, D. G. (1982) ‘On the Slope-Aspect Correction of Multispectral Scanner Data’, Canadian Journal of Remote Sensing, 8(2), pp. 84–106. doi: 10.1080/07038992.1982.10855028.
