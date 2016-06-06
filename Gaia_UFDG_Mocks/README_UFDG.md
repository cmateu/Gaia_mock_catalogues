Ultra-Faint Dwarf Galaxy Mock Gaia Catalogues
======

**DESCRIPTION:**

This repository contains catalogues from Antoja et al. 2015 (MNRAS, 453, 541) for a library of synthetic Ultra-Faint Dwarf Galaxies (UFDG). The simulation of Gaia errors, stellar population model and distribution of parameters for the UFDGs are explained in detail in Antoja et al. 2015.

Each UFDG is simulated as a simple stellar population, with an age of 12Gyr and metallicity [Fe/H]=-1.5, binary stars are included following the model of Hernandez-Perez \& Bruzual 2014. UFDGXs are distributed logarithmically in (heliocentric) distance from 10 to 250 kpc. Each UFDG is simulated with a different half-light radii, velocity dispersion, total luminosity and center of mass velocity drawn at random. The distributions and ranges assumed for these parameters are summarized in Table 1 and Sec. 2 of Antoja et al. 2015.


**FILE STRUCTURE**

Two types of files are included: truep.* and obs.* files. The first contain error-free parameters and the second error-convolved parameters, assuming post-launch Gaia error prescriptions from de Bruijne, Rygl \& Antoja 2014.

The files in the GitHub repository (as of 04 June 2016) are a subset of 1000 UFDGs out of the total 10000 used in Antoja et al. 2015. The full UFDG library is available upon request to Cecilia Mateu (cmateu @ cida.gob.ve) or Teresa Antoja (tantoja @ cosmos.esa.int) and will be made available soon through a public ftp server.

The structure of the files is as follows:

FB - Flag to indicate whether star is isolated (0), part of a resolved binary (1) or unresolved binary (1) 
alpha(deg),delta(deg) - Equatorial coordinates (degree)
mualpha(mas/yr),mudelta(mas/yr) - Proper motions in equatorial coordinates. Mualpha is reduced proper motion (mu*cos(delta).
distance(pc) - Heliocentric distance (pc)
radVelocity(km/s) - Radial velocity. Null value is 99999. Stars in binaries are assigned null radial velocities.
MeanAbsV - Absolute magnitude in the V-band
G,Gb,Grp - Gaia G-band, G_BP and G_RP band magnitudes. For stars in unresolved binaries these are combined magnitudes.
intVMinusI - Intrinsic V-I colour
teff - Effective temperature (null for binaries)
logG - Surface gravity (null for binaries)
feh - Iron abundance [Fe/H]
age - Assumed age for the stellar population
Av  - V-band Extinction 

