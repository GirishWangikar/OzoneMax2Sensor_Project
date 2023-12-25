### Readme

This repository comprises various components essential for multimodal data analysis and prediction of gene expression using recurrent neural networks (RNNs) and autoencoders (AEs).

#### Contents:

1. **AutoEncoder Results:** Contains code for the AutoEncoder model, generating latent space representations for electrical data across defined intervals (-60 to 0, 0 to 15, 15 to 30, and 30 to 60) for metrics such as Peaks, RMS, CrestFactor, and AverageFrequency. The folder also includes comparison results between AutoEncoder latent space and raw averaged electrical data for different lines and replicates.

2. **Latent Space Representation:** Holds the AutoEncoder latent space representations for various metrics in xlsx format.

3. **Codes:** Contains RNN codes (`RNN+AE C_Line`, `RNN+AE S_Line`, `RNN+AE WT_Line`) used along with their corresponding weights for modeling both with and without electrical components.

4. **Input Data:** Includes input data for C, S, and WT lines, as well as FPKM (gene expression) data.

5. **Reference Papers:** A list of references utilized during code implementation.

6. **Results:** Holds various results such as bar graphs, flowcharts, RMSE comparisons with and without electrical data, and the impact of scrambled electrical data on predictions. Additionally, it contains a database of differentially expressed genes (DEGs) for validation.

7. **Weights:** Consists of weights of tensors used in the codes (e.g., `X` - concatenated data at 0, 15, and 30 minutes, and `Y` - ground truth data consisting of 60-minute values).

#### Code Dependencies:

The code relies on the following Python packages:

```python
import pandas as pd
import numpy as np
import os
import copy
from sklearn.preprocessing import minmax_scale
from scipy.stats import zscore
import torch
import torch.nn as nn
from torch.autograd import Variable

These packages are fundamental for data manipulation, preprocessing, neural network implementation, and tensor operations throughout the analysis.

Please refer to specific folders/files within this repository for detailed code implementations, data, and results.
