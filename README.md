<div align="center">

# Deep Learning Reproductions

[![python](https://img.shields.io/badge/-Python_3.11-blue?logo=python&logoColor=white)](https://github.com/pre-commit/pre-commit)
[![pytorch](https://img.shields.io/badge/PyTorch_2.0+-ee4c2c?logo=pytorch&logoColor=white)](https://pytorch.org/get-started/locally/)
[![lightning](https://img.shields.io/badge/-Lightning_2.0+-792ee5?logo=pytorchlightning&logoColor=white)](https://pytorchlightning.ai/)
[![hydra](https://img.shields.io/badge/Config-Hydra_1.3-89b8cd)](https://hydra.cc/)<br>
[![tests](https://github.com/avansp/dl-repro/actions/workflows/test.yml/badge.svg)](https://github.com/avansp/dl-repro/actions/workflows/test.yml)
[![code-quality](https://github.com/avansp/dl-repro/actions/workflows/code-quality-main.yaml/badge.svg)](https://github.com/ashleve/lightning-hydra-template/actions/workflows/code-quality-main.yaml)
[![license](https://img.shields.io/badge/License-MIT-green.svg?labelColor=gray)](https://github.com/avansp/dl-repro#license)

</div>

## Collections

My collection of DL models' reproduction codes.

## Installation

#### Pip

```bash
# clone project
git clone https://github.com/YourGithubName/your-repo-name
cd your-repo-name

# [OPTIONAL] create conda environment
conda create -n myenv python=3.9
conda activate myenv

# install pytorch according to instructions
# https://pytorch.org/get-started/

# install requirements
pip install -r requirements.txt
```

#### Conda

```bash
# clone project
git clone https://github.com/YourGithubName/your-repo-name
cd your-repo-name

# create conda environment and install dependencies
conda env create -f environment.yaml -n myenv

# activate conda environment
conda activate myenv
```

