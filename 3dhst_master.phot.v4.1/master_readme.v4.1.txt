Master Catalog
##################

Known Issues 
^^^^^^^^^^^^^^^

The following are the currently known issues:

* The abbreviations for the GOODS-N and GOODS-S fields in the master photometric catalog are both "g". We suggest the use of RA and Dec alone or in combination with the "field" column to select object from either field.

Catalog
^^^^^^^^^^^^^^^

We combine the catalogs for the five individual fields into a master catalog which contains a subset of parameters
common to all of them. This joint catalog is provided in both ASCII and FITS format. Below we show the header
for this file and a description of the columns. The id column in this catalog is no longer unique. An unique identifier 
can be created from a combination of the id and the field name.

::

	# id field ra dec x y z_spec z_peak faper_F140W eaper_F140W faper_F160W eaper_F160W f_F606W 
	e_F606W f_F814W e_F814W f_F125W e_F125W f_F140W e_F140W f_F160W e_F160W tot_cor kron_radius 
	a_image b_image flux_radius fwhm_image flags f140w_flag star_flag use_phot near_star 
	nexp_f125w nexp_f140w nexp_f160w lmass Av

All fluxes are normalized to an AB zeropoint of 25, such that: magAB = 25.0-2.5*log10(flux).


========================  ==============================================================================
Column Name                                Column Content
========================  ==============================================================================
1    # id					Unique identifier within a given field  	
2    # field				Field
3    # x					X centroid in image coordinates
4    # y					Y centroid in image coordinates  
5    # ra					RA J2000 degrees 
6    # dec					Dec J2000 degrees   
7    # z_spec         		Spectroscopic redshift, when available see Skelton et al., 2014 for sources 
8    # z_peak				Photometric redshift from EAZY fit
9    # faper_F160W			Flux within a 0.7 arcsecond aperture in F160W zeropoint 25.0 	  
10   # eaper_F160W			1 sigma error within a 0.7 arcsecond aperture in F160W zeropoint 25.0 
11   # faper_F140W			Flux within a 0.7 arcsecond aperture in F140W zeropoint 25.0 		  
12   # eaper_F140W			1 sigma error within a 0.7 arcsecond aperture in F140W zeropoint 25.0 	  
13   # f_F160W				Total flux in F160W zeropoint 25 	  
14   # e_F160W				1 sigma error in F160W total flux zeropoint 25 	  
15   # w_F160W				Weight relative to 95th percentile within F160W weight map
16   # f_F606W        		Total flux in F606W zeropoint 25 						  
17   # e_F606W				1 sigma error in F606W total flux zeropoint 25 				  
18   # w_F606W        		Weight relative to 95th percentile within F606W weight map
19   # f_F814W        		Total flux in F814W zeropoint 25 
20   # e_F814W				1 sigma error in F814W total flux zeropoint 25 
21   # w_F814W        		Weight relative to 95th percentile within F814W weight map 	
22   # f_F125W        		Total flux in F125W  zeropoint 25 
23   # e_F125W				1 sigma error in F125W  total flux zeropoint 25 
24   # w_F125W        		Weight relative to 95th percentile within F125W weight map
25   # f_F140W        		Total flux in zeropoint 25 
26   # e_F140W				1 sigma error in  total flux zeropoint 25 
27   # w_F140W        		Weight relative to 95th percentile within weight map
28   # f_F160W				Total flux in F160W zeropoint 25 	  
29   # e_F160W				1 sigma error in F160W total flux zeropoint 25 	  
30   # w_F160W				Weight relative to 95th percentile within F160W weight map			  
31   # tot_cor        		Correction from AUTO to total flux based on F160W F140W 
32   # kron_radius    		KRON_RADIUS 
33   # a_image				A_IMAGE semi-major axis, pixels 
34   # b_image				B_IMAGE semi-minor axis, pixels 
35   # class_star     		Sextractor stellarity-index CLASS_STAR 
36   # flux_radius    		Circular aperture radius enclosing half the total flux
37   # fwhm_image     		FWHM pixels  from a gaussian fit to the core
38   # flags				SExtractor extraction flags measured
39   # f140w_flag			Set if F140W is used for the corrections to total i.e., no F160W coverage 
40   # star_flag      		For F160W<25, star=1 and galaxy=0; for F160W>25, flag=2
41   # use_phot				Use flag: 1=USE, 0=DON'T USE; see Skelton et al. 2014  for definition
42   # near_star			1=Close to a star
43   # nexp_f125w			Number of individual exposures in F125W, based on NEXP maps
44   # nexp_f140w			Number of individual exposures in F140W, based on NEXP maps
45   # nexp_f160w			Number of individual exposures in F160W, based on NEXP maps
46   # lmass				LogMstar/Msun  from FAST fit
47   # Av					Dust attenuation in the V-band from FAST fit
========================  ==============================================================================

