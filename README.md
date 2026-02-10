# espectroXAS_ML: Physics-gated CNN for high-throughput O K-edge.
An implementation of a 1D-Convolutional Neural Network (CNN) designed to predict Oxygen K-edge spectra in transition metal oxides using ground-state DFT descriptors.

## Physical Framework
The model incorporates a **Physics Gate** in the loss function to ensure that spectral transitions are constrained by the local $p$-$d$ hybridization:

$$\mathcal{L} = \| y_{ML} - y_{True} \|^2 + \lambda \int |y_{ML}(\omega) \cdot (1 - \text{Gate}(\omega))| \, d\omega$$

## Project Structure
- `/src`: Modularized source code for features, architecture, and utils.
- `/models`: Serialized Keras models.
- `/plots`: Automated benchmarking plots against BSE and Experiment.

## Installation
```bash
pip install -r requirements.txt
