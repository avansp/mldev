<div align="center">

# Machine Learning Dev Template

[![python](https://img.shields.io/badge/-Python_3.11-blue?logo=python&logoColor=white)](https://github.com/pre-commit/pre-commit)
[![pytorch](https://img.shields.io/badge/PyTorch_2.0+-ee4c2c?logo=pytorch&logoColor=white)](https://pytorch.org/get-started/locally/)
[![lightning](https://img.shields.io/badge/-Lightning_2.0+-792ee5?logo=pytorchlightning&logoColor=white)](https://pytorchlightning.ai/)
[![hydra](https://img.shields.io/badge/Config-Hydra_1.3-89b8cd)](https://hydra.cc/)<br>
[![tests](https://github.com/avansp/mldev/actions/workflows/test.yml/badge.svg)](https://github.com/avansp/mldev/actions/workflows/test.yml)
[![code-quality](https://github.com/avansp/mldev/actions/workflows/code-quality-main.yaml/badge.svg)](https://github.com/avansp/mldev/actions/workflows/code-quality-main.yaml)
[![license](https://img.shields.io/badge/License-MIT-green.svg?labelColor=gray)](https://github.com/avansp/dl-repro#license)

This is a simplified template derived from [@ashleve's lightning-hydra-template](https://github.com/ashleve/lightning-hydra-template).

</div>

## Installation

<details>
<summary><b>pip</b></summary>

```bash
# clone project
git clone https://github.com/avansp/mldev.git
cd mldev

# create conda environment
conda create -n mldev python=3.9
conda activate mldev

# install pytorch according to instructions
# https://pytorch.org/get-started/

# install requirements
pip install -r requirements.txt
```

</details>

<details>
<summary><b>conda</b></summary>

```bash
# clone project
git clone https://github.com/avansp/mldev.git
cd mldev

# create conda environment and install dependencies
conda env create -f environment.yaml -n mldev

# activate conda environment
conda activate mldev
```

</details>

<details>
<summary><b>testing</b></summary>

```bash
# run all tests
pytest

# run tests from specific file
pytest tests/test_train.py

# run all tests except the ones marked as slow
pytest -k "not slow"
```

</details>

## Run with `Makefile`

The easiest way to run is by using `make` command:

```bash
# Show what commands available
make help
```

## Training

> :*Note*: all outputs are saved in logs directory with the model name.

MNIST is a default model when you just run train / eval / predict without a specific configuration, or
you can also run the experiment defined in `mnist_train.yaml`:

```bash
# see configs/experiment/mnist_train.yaml
python src/train.py experiment=mnist_train data.num_workers=20
```

There is also an example of using multiruns to search optimal hyper-parameters:

```bash
# use multirun -m switch
python src/train -m hparams_search=mnist_optuna experiment=mnist_train data.num_workers=20
```
