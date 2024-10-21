# Sparse LInear Multiple Kernel Learning (SLIM-KL)

This repository contains the code and data used in the paper ["Sparsity-Aware Distributed Learning for Gaussian Processes with Linear Multiple Kernel"](https://arxiv.org/abs/2309.08201).

## Citation
```
@article{suwandi2023gaussian,
  title={Sparsity-Aware Distributed Learning for Gaussian Processes with Linear Multiple Kernel},
  author={Richard Cornelius Suwandi and Zhidi Lin and Feng Yin and Zhiguo Wang and Sergios Theodoridis},
  journal={arXiv preprint arXiv:2309.08201},
  year={2023}
}
```

## Example
To see an example, please run the `main.m` file. To change the data set, simply uncomment one of the listed data sets and comment the others, e.g., for the `unemployment` data set,
```
file_name = 'unemployment';
% file_name = 'CO2';
% file_name = 'ECG_signal';
% file_name = 'ale80';
% file_name = 'airfoil600';
% file_name = 'cccp1000';
% file_name = 'toxicity436';
% file_name = 'concrete824';
% file_name = 'water800';
% file_name = 'wine1279';

disp(['Simulation on ',file_name]);
[xtrain, ytrain, xtest, ytest] = load_data(file_name);
nTrain = length(xtrain);
nTest = 20;
```
Other algorithm setups can also be changed in the corresponding files.

## Dependencies
The current version of the code uses MATLAB R2021a (https://www.mathworks.com/products/matlab.html) and MOSEK version 9.3 (https://docs.mosek.com/9.3/install/installation.html). Please refer to the corresponding websites for the installation instructions.
