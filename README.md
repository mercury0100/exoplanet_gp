# exoplanet_gp

Modelling TESS lightcurves and exoplanetary transits with Gaussian Process regression

We use a simple harmonic oscillator kernel to model the intrinsic asteroseismic oscillation of the star, in linear combination with a jitter term, with normally distributed prior in log space, to capture misspecified error bars and model misspecification, and a mean constant flux with normal prior centred at zero. The harmonic oscillator has three parameters: the quality factor Q, the central frequency ω and the amplitude a. Each parameter is given a Gaussian prior in log space.

To estimate the power excess of the modes we calculate the Mean Collapsed Correlation (MCC, see Kiefer 2013, Viani et al. 2019) . The MCC metric is convolved with an AstroPy Gaussian 1D Kernel smooth it, and the peak frequency of the smoothed MCC is used as a prior estimate of the dominant frequency ω.
