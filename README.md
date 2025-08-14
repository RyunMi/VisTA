<h1 align="center">Cross-Domain Attribute Alignment with CLIP: A Rehearsal-Free Approach for Class-Incremental Unsupervised Domain Adaptation</h1>

<p align="center">
  <strong>Official implementation of VisTA framework.</strong><br>
  ACM International Conference on Multimedia (ACM MM), 2025
  
</p>

---

## Overview
This repository introduces **VisTA**, a rehearsal-free framework for Class-Incremental Unsupervised Domain Adaptation (**CI-UDA**):

- VisTA leverages CLIP to mine and preserve domain-invariant and class-agnostic knowledge to facilitate CI-UDA.

- VisTA effectively reduces catastrophic forgetting while mitigating the domain shift, guided by an Attribute Modeling module, a Visual Attention Consistency module, and a Prediction Consistency loss.

<div align="center">
  <img src="assets/VisTA.png" width="900px" />
</div>

## Installation 
Our code is implemented in Python (version >= 3.8) with PyTorch (version >= 1.11.0). Please follow the steps below to configure dependencies:
```bash
# Install CLIP
git clone https://github.com/openai/CLIP.git
cd CLIP
pip install .

# Install Dassl
git clone https://github.com/KaiyangZhou/Dassl.pytorch.git
cd Dassl.pytorch
pip install -r requirements.txt
pip install .

# Install other dependent packages of VisTA.
git clone https://github.com/RyunMi/VisTA.git
cd VisTA
pip install -r requirements.txt
```

## Datasets
Please follow the [instructions](https://github.com/KaiyangZhou/Dassl.pytorch/blob/master/DATASETS.md) to prepare three datasets for CI-UDA: Office-31, Office-Home, and Mini-DomainNet. After preparing the datasets, please update the `DATA` variable in `scripts/{dataset}.sh` accordingly.

## Training
For CI-UDA, we provide scripts to run experiments:

```bash
# Training on Office-31
sh scripts/office31.sh

# Training on Office-Home
sh scripts/officehome.sh

# Training on Mini-DomainNet
sh scripts/minidomainnet.sh
```

## Appendix

The supplementary materials are available [here](https://github.com/RyunMi/VisTA/blob/main/assets/Supplementary.pdf).

## Citation
If you find the code useful in your research, please consider citing:

```bibtex
@inproceedings{VISTA,
author = {Mi, Kerun and Kang, Guoliang and Li, Guangyu and Zhao, Lin and Zhou, Tao and Gong, Chen},
title = {Cross-Domain Attribute Alignment with CLIP: A Rehearsal-Free Approach for Class-Incremental Unsupervised Domain Adaptation},
year = {2025},
booktitle = {Proceedings of the 33rd ACM International Conference on Multimedia},
pages = {},
numpages = {10},
series = {MM '25}
}
```

## Acknowledgments

Thanks sincerely for the following projects:

[CoOp](https://github.com/KaiyangZhou/CoOp)

[DAPrompt](https://github.com/LeapLabTHU/DAPrompt)

[AttriCLIP](https://github.com/vanity1129/AttriCLIP)