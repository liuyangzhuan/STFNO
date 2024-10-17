# STFNO
STFNO Copyright (c) 2024, The Regents of the University of California, through Lawrence Berkeley National Laboratory (subject to receipt of any required approvals from the U.S. Dept. of Energy).  All rights reserved.

## Overview
STFNO (Sparsified Time-dependent PDEs FNO code) is an extension of the popular Fourier Neural Operator (FNO) architecture to the solution of coupled systems of time-dependent partial differential equations. STFNO leverages the sparsified dependencies on the field quantities based on the semi-discretiezed form of the PDEs, enabling significant reduction in the number of model parameters. STFNO has been extensively tested on two fusion simulation codes, NIMROD and GTC, and can be easily tailored to other systems of PDEs. STFNO is a fully Python code and depends on pytorch and numpy.  

## Getting Started 
STFNO has two examples to demonstrate its usage, located at examples/NIMROD2D and examples/GTC2D. These examples require pre-generated datasets using the NIMROD and GTC codes. We have made one of our NIMROD datasets available at https://zenodo.org/records/13901806 generated by the NIMROD code https://nimrodteam.org/, and the other datasets are also available upon request. To use the dataset:
```
git clone https://github.com/liuyangzhuan/STFNO.git
cd STFNO
cd examples/NIMROD2D
export PYTHONPATH=<path of stfno directory>:$PYTHONPATH
download the dataset from https://zenodo.org/records/13901806
set path_data_read = <path of the downloaded dataset> in main.py (with the default: if_HyperDiffusivity_case=True, if_2ndRunHyperDiffusivity_case=True, S=64) 
python main.py
```

## Current developers
 - Mustafa Rahman - rahman@lbl.gov (Lawrence Berkeley National Laboratory)  
 - Yang Liu - liuyangzhuan@lbl.gov (Lawrence Berkeley National Laboratory) 

## Reference
