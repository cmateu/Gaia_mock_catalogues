Warped Disk Gaia Mock Catalogues 
======

**DESCRIPTION:**

This repository contains catalogues from Abedi et al. 2014 (MNRAS, 442, 3627). These are Gaia mock catalogues made from test particle simulations in adiabatically warped potentials. 

For full details on how the simulations were produced and Gaia errors simulated, please see Secs. 2 and 3 in `Abedi et al. (2014) <http://adsabs.harvard.edu/abs/2014MNRAS.442.3627A>`__.

The file names follow this syntax: OBEE27_p0.qt1.dat.

The first two letters denote the stellar tracer used. OB, AA and RC denote respectively Main Sequence OB stars, Main Sequence A stars and Red Clump giants.
EE27 indicates the catalogue includes only Gaia observable stars (G<20) and the warp model maximum tilt angle is 27 deg (at a distance of 20 kpc). The tilt angle dependence upon galactocentric distance (r) is given in Eq. 2 of Abedi et al. 2014.
p0 indicates the model without twisting of the line of nodes.
qt1 indicates this is a random sample with one quarter of the total number of stars expected. Table 2 in Abedi et al. 2014 summarizes

Note: The full catalogues are available upon request to cmateu @ cida.gob.ve. We will soon make the publicly available through an ftp repository.

**FILE STRUCTURE**

The structure of the catalogues is the following:

- Av, V, Gmag, Grvs : V-band extinction; V-band, G and Grvs apparent magnitudes
- xX,xY,xZ,xVX,xVY,xVZ : error-free cartesian galactocentric coordinates (kpc) and velocities (km/s)
- xl_deg,xb_deg,xRhel_kpc,xmulcosb_masyr,xmub_masyr,xvrad : error-free observables (l,b, heliocentric distance in kpc, proper motions in mas/yr, radial velocities in km/s)
- gX,gY,gZ,gVX,gVY,gVZ : error-convolved cartesian galactocentric coordinates and velocities.
- gl_deg,gb_deg,gRhel_kpc,gmulcosb_masyr,gmub_masyr,xvrad : error-convolved observables
- VI: Observed (V-I)c colour
