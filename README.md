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

## Installation

#### Pip

```bash
# clone project
git clone https://github.com/avansp/dl-repro.git
cd dl-repro

# create conda environment
conda create -n dl-repro python=3.9
conda activate dl-repro

# install pytorch according to instructions
# https://pytorch.org/get-started/

# install requirements
pip install -r requirements.txt
```

#### Conda

```bash
# clone project
git clone https://github.com/avansp/dl-repro.git
cd dl-repro

# create conda environment and install dependencies
conda env create -f environment.yaml -n dl-repro

# activate conda environment
conda activate dl-repro
```

#### Testing

```bash
# run all tests
pytest

# run tests from specific file
pytest tests/test_train.py

# run all tests except the ones marked as slow
pytest -k "not slow"
```

## Collections

> :*Note*: all outputs are saved in logs directory with the model name.

<details>
<summary><b>MNIST</b></summary>

This is a default model when you just run train / eval / predict without a specific configuration, or
you can also run the experiment defined in mnist_train:

```bash
# see configs/experiment/mnist_train.yaml
python src/train.py experiment=mnist_train data.num_workers=20
```

There is also an example of using multiruns to search optimal hyperparameters:

```bash
# use multirun -m switch
python src/train -m hparams_search=mnist_optuna experiment=mnist_train data.num_workers=20
```

See also:

* **Data**: `configs/data/mnist.yaml`
* **Model**: `configs/model/mnist.yaml`

</details>
