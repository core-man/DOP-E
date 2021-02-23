# DOP-E package

Created by Andrea Berbellini, November 2018
For questions, bugs, comments please email me: andrea.berbellini@ingv.it

The goal of this package is to measure Rayleigh wave ellipticity from the
polarization of ambient noise and to invert it to constrain S-wave velocity,
as in Berbellini et al. 2019.

We provide this package to reproduce our results.

It is formed of two main folders:
Measurement: 	Containing the main DOP-E routines to measure ellipticity of Rayleigh waves from ambient noise.
		We provide one month of data from Concordia station (CCD, Antarctica) in January 2009, already cut
		in chunks of 8162 samples and corrected for the instrument response. See the README in the
		measurement folder for more details and references

Inversion:	Here we provide two versions of the code:

	Serial: 	To run inversion on a laptop or pc. A single inversion in this particular case takes approx 1 hour time,
			but the computational time increases rapidly if a more complex parameterisation for the crust is used,
			i.e. with more layers.

	Parallel:	The parallel version of the code. Very similar to the serial version, it can run on clusters. In our case
			we always run this version using 20 cpu. In this case an inversion takes approx 15 minutes for 4500 models.



## Citations

This software is free to download. If used please cite:

Berbellini, A., Schimmel, M., Ferreira, A.M.G., Morelli, A.,
    	Constraining S-wave velocity using Rayleigh wave ellipticity
    	from polarization analysis of seismic noise, Geophysical Journal
    	International,  Volume 216, Issue 3, 1 March 2019, Pages 1817–1830,
	https://doi-org.eres.qnl.qa/10.1093/gji/ggy512

The DOP-E method is an update of the method implemented byMartin Schimmel:
	Schimmel, M. & Gallart, J., 2004. Degree of polarization filter for frequency-dependent
	signal enhancement through noise suppression, Bull. Seismol. Soc. Am., 94(3), 1016–1035.

	Schimmel, M., Stutzmann, E., Ardhuin, F., & Gallart, J., 2011. Polarized Earth’s ambient
	microseismic noise, Geochemistry, Geophys. Geosystems, 12(7), 1–14.

The inversion is based on the software created by Malcolm Sembridge:
	Sambridge, M., 1999. Geophysical inversion with a neighbourhood algorithm-I.
	Searching a parameter space, Geophysical Journal International, 138(2), 479–494.

The forward modeling is based on the package "Computer Programs in Seismology" by Robert B. Hermann:
	Herrmann, R. B., 2013. Computer Programs in Seismology: An Evolving Tool for
	Instruction and Research, Seismol. Res. Lett., 84(6), 1081–1088.

