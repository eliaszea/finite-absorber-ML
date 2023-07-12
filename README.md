# finite-absorber-ML
Datasets, models, and results for the paper "Sound absorption estimation of finite porous samples with deep residual learning"[^1]. 

**1. INTRODUCTION**

This repository contains the models and data to reproduce the paper's results[^1]. In that paper, residual neural networks perform at least as well as the two-microphone method for frequencies above 1 kHz and significantly better than it for small absorbers and frequencies below 400 Hz. It could be said that the neural networks are trained to detect strong edge diffraction and mitigate it from the measurement. 

[^1]: [E. Zea, E. Brand ̃ao, M. Nolan, J. Cuenca, J. And ́en, and U. P. Svensson. Sound absorption
estimation of finite porous materials with deep residual learning. Preprint submitted to The
Journal of the Acoustical Society of America, DOI: 10.13140/RG.2.2.19369.88165, July 2023](http://dx.doi.org/10.13140/RG.2.2.19369.88165).

`finite-absorber-ML` is covered by a GPL v3 license (see LICENSE for license terms).

**2. INSTALLATION**

Download the .zip file and extract it in your folder of preference. To run the scripts locally, the user must have installed the following Python packages:

- `Numpy`
- `Keras`
- `TensorFlow`
- `Pickle`
- `Pandas`
- `Matplotlib`

**3. DATASETS**

The datasets can be found in [Zenodo](https://doi.org/10.5281/zenodo.8137012)[^2]. The user should download them to their local/cloud environment. The sound fields are generated with a simplified boundary element method (BEM) of a baffled porous layer on a rigid backing using the Delany–Bazley–Miki[^3] model. There are 330k simulations, out of which 300k are for training and validation sets (80/20 %), 15k for an interpolation test set, and another 15k for an extrapolation test set. 

The paper uses the training and validation datasets to train the neural networks. The test sets assess the network's performance against unseen data.

[^2]: [Zea et al. 2023, Dataset of sound field simulations above finite absorbers, Zenodo, DOI: 10.5281/zenodo,8137012](https://doi.org/10.5281/zenodo.8137012).
[^3]: [Y. Miki, “Acoustical properties of porous materials-modifications of Delany-Bazley models,” J. Acoust. Soc. Japan (E) 11(1), 19–24 (1990).](https://www.jstage.jst.go.jp/article/ast1980/11/1/11_1_19/_article/-char/ja/).


**4. PYTHON SCRIPTS**

Two scripts are provided: (These are not published yet, come back again soon!)

_4.1. trainModels.py_

This script can be run to train the models from scratch. The default training settings are taken from the paper by Zea et al. (2023). To modify these settings, the user must choose the training parameters, such as `batchSize`, `optimizer`, etc. 

_4.2 reproduceFigures.py_

This script can be used to reproduce the results figures in the paper by Zea et al. (2023). 

**5. RELEASE HISTORY**

	Release #1	 finite-absorber-ML v1.0 	E. Zea	2023-07-12

**6. FEEDBACK & CONTACT INFORMATION**

Your questions, suggestions, and feedback can help improve the quality of this software. Feel free to contact me at

	Elias Zea (zea@kth.se)
	Marcus Wallenberg Laboratory for Sound and Vibration Research
	Department of Engineering Mechanics
	KTH Royal Institute of Technology
	Teknikringen 8
	10044 Stockholm, SWEDEN

**7. LEGAL INFORMATION**

Copyright 2023 Elias Zea, Eric Brandão

This software was written by Elias Zea, and the datasets were created by Eric Brandão. 

`finite-absorber-ML` is free software. You can redistribute it and/or modify it under the
terms of the GNU General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version. If not stated otherwise, this applies to all files contained in this package and its sub-directories. 

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307  USA
