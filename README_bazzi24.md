## Create venv with python 3.7
```bash
conda create -n ebm_env_venv python=3.7
```
Active venv
```bash
conda activate ebm_env_venv
```
## Install Torch
```bash
conda install pytorch=0.4.1 torchvision=0.2.1 -c pytorch
```
Install dependencies and library
```bash
pip install -r reuirements.txt
```
## If you use CPU and do not use NVDIA --> Remove cuda
```bash
find scripts/ -name "*.py" -exec sed -i 's/\.cuda()//g' {} +

find data/ -name "*.py" -exec sed -i 's/\.cuda()//g' {} +
```
