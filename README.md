# Izhikevich Neuron Model Simulation

This repository contains a Python implementation of the Izhikevich neuron model to simulate Regular Spiking (RS) neurons.


## Table of Contents

* [Introduction](#introduction)
* [Requirements](#requirements)
* [Code Structure](#code-structure)
* [How the Code Works](#how-the-code-works)
* [Running the Notebook](#running-the-notebook)
* [Example Plots](#example-plots)
* [References](#references)


## Introduction

The Izhikevich neuron model is a mathematical representation of cortical spiking neurons. This simulation studies the RS neuron's response to varying external input levels.


## Requirements

* Python 3.x
* NumPy
* Matplotlib
* Jupyter Notebook


## Code Structure

* `Izhikevich.ipynb`: Interactive Jupyter Notebook for simulation and plotting


## How the Code Works

### Imports

The code starts by importing necessary libraries:


* `numpy` for numerical computations
* `matplotlib.pyplot` for plotting


### Izhikevich Model Implementation

The Izhikevich model is implemented using two coupled differential equations:


* Equation (1): `dv/dt = 0.04v^2 + 5v + 140 - u + I(t)`
* Equation (2): `du/dt = a(bv - u)`


with the condition:


* `if v >= 30, v = c, u = u + d`


### Simulation Parameters

The simulation parameters are:


* `a`, `b`, `c`, `d`: Izhikevich model parameters
* `I_values`: array of external input levels
* `steps`: number of simulation steps
* `tau`: time step


### Simulation Loop

The simulation loop iterates over:


* External input levels (`I_values`)
* Time steps (`steps`)


### Plotting

The code generates two plots:


* Membrane potential time-series for varying input levels
* Mean spike rate vs. input level plot


## Running the Notebook

1. Clone the repository: `git clone https://github.com/fardeen0424/Izhikevich-Neuron-Model-Simulation`
2. Install required libraries: `pip install numpy matplotlib`
3. Run Jupyter Notebook: `jupyter notebook Izhikevich.ipynb`
4. Follow instructions in the notebook to simulate and plot RS neuron behavior


## Example Plots

* Membrane potential time-series for varying input levels

* ![Untitled](https://github.com/user-attachments/assets/557ae02d-8e83-4e3b-a774-3fab580ede4a)

* Mean spike rate vs. input level plot

![Untitled-1](https://github.com/user-attachments/assets/56f9f796-4ce6-4645-b1cb-1fa955213a06)


## References

* Izhikevich, E. M. (2003). Simple model of spiking neurons. IEEE Transactions on Neural Networks, 14(6), 1569-1572.
* Izhikevich, E. M. (2004). Which model to use for cortical spiking neurons? IEEE Transactions on Neural Networks, 15(5), 1063-1070.

