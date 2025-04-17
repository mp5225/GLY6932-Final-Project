# GLY6932-Final-Project
A simple neural network for detecting exoplanet transits

The jupyter notebook in this repository contains code for creating simple NN with tensorflow for detecting exoplanet transits in light curve data.
Transits occur when a planet passes directly in front of its host star when seen from Earth. This produces a slight dimming of the star's light,
which is proportional to the square of the planet/star radius ratio. Transits have been used to detect thousands of exoplanets, mainly thanks to the
Kepler and TESS satellites. In practice, transit light curve data comes in the form of light curves. A light curve is a series of flux measurements,
typically taken once every few minutes over several hours or days. For this project, I created 20,000 synthetic light curves, and trained a neural net
to pick out which ones have transits in them.

The code contains the framework to generate new data. If you would like to use the existing data I have included in this repo, you do not need to run
the first two cells. Instead, simply run the cell that loads lightcurves.txt and true_lightcurves.txt. If you WOULD like to create your own data,
you can run the first cell. If you would like to adjust the amount of data or the planet generation parameters, you can do so by modifying a_max, a_min,
N_transits, etc in this cell.

The model has a set random seed so that the same result can be produced each time, given the same input data. With the pre-uploaded data, the model
achieves 99% accuracy. By default has 5 layers: an input layer, 3 dense layers with a reLU activation, and an output with a sigmoid activation. the
user can adjust these or modify the model in the cell commented #create model.
