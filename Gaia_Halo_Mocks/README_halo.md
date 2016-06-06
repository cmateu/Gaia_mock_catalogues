Haloes Gaia Mock Catalogues
======

**DESCRIPTION:**

This repository contains catalogues from Mateu et al. 2016 (in prep.), simulating Gaia observable K giant and RR Lyrae stars from the Aquarius A2-E2 haloes, extracted from the Aquarius Database (Lowing et al. 2015) mock catalogues. Gaia errors are simulated using the latest post-launch error prescriptions from de Bruijne, Rygl & Antoja (2014). Stellar streams are identified in these catalogues using the mGC3 methods, a family of great-circle cell methods introduced in Mateu et al. 2011 (MNRAS, 415, 214) and expanded in Abedi et al. (2014, MNRAS 442, 3627). 

For full details on how the simulations were produced and Gaia errors simulated, please see the III Gaia Challenge website (http://astrowiki.ph.surrey.ac.uk/dokuwiki/doku.php?id=tests:streams:challenges#error-convolved_mock_catalogue_of_individual_halo_stellar_tracers).

**FILE STRUCTURE**

Catalogues:
-------------

Mock catalogues are provided in two types of directories: AquariusA2_KIII_pe_byIDstream and AquariusA2_KIII_pe_byIDpole.
The directory names indicate the Aquarius halo they correspond to (Aquarius A2 in this example) and the stellar tracer (KIII or RRLS). Inside *IDstream directories, stars are saved in files according to their IDstream, a unique ID that identifies the progenitor each star belonged to when accreted into the main halo. The *IDpole directories give the stars associated to each of the poles detected in nGC3 pole count map of the corresponding Halo (See Sec. Finding Streams in the Halo in http://astrowiki.ph.surrey.ac.uk/dokuwiki/doku.php?id=tests:streams#finding_streams_in_the_halo). These files represent realistic tidal stream detections, in the sense that they include Gaia observational errors, there will be missing stars and stars from more than one progenitor can be included in any given pole detection.

Each of the files provided has the following structure:

- Av, V, Gmag, Grvs : V-band extinction, V-band, G and Grvs apparent magnitudes
- xX,xY,xZ,xVX,xVY,xVZ : error-free cartesian galactocentric coordinates (kpc) and velocities (km/s)
- xl_deg,xb_deg,xRhel_kpc,xmulcosb_masyr,xmub_masyr,xvrad : error-free observables (l,b, heliocentric distance in kpc, proper motions in mas/yr, radial velocities in km/s)
- gX,gY,gZ,gVX,gVY,gVZ : error-convolved cartesian galactocentric coordinates and velocities.
- gl_deg,gb_deg,gRhel_kpc,gmulcosb_masyr,gmub_masyr,xvrad : error-convolved observables
- IDstream: progenitor ID. Stars with same IDstream come were accreted in the same progenitor.
- IDpole: pole detection label in pole-count map.

The catalogues provided contain the full sample of stars for each halo. Catalogues are provided only for Aquarius A2 and C2 haloes. The B2, D2 and E2 haloes, as well as analogous catalogues for 6 EAGLE-zoom haloes are available upon request to cmateu @ cida.gob.ve. We will soon make the publicly available through an ftp repository.

Library logs:
-------------

Log files are provided for the mock catalogues describing the parameters of the progenitors in each simulated halo. Log file names follow a similar syntax as the catalogues, indicating the halo and tracer (AquariusA2KIII.IDstream.extended.GMM.log).

The log files contain the following information:

- IDstream -  progenitor ID. Stars with same IDstream come were accreted in the same progenitor.
- TreeID   -  progenitor ID used in the Aquarius Database
- infallZ  -  redshift at which the progenitor was accreted by the main halo
- mlogage_yr - mean log age of the stellar population of the progenitor
- mZmetal    - mean Z metallicity  of the stellar population of the progenitor
- Ntrc_ne    - total number of tracer stars in the progenitor (with G<20, no extinction)
- Ntrc_pe    - number of Gaia observable stars (G<20, considering extinction and errors)
- Ntrc_pe    - number of Gaia observable stars with proper motion errors <50%
- dtheta_pe  - angular width of the progenitor (perpendicular to the orbital plane in the case of streams)

