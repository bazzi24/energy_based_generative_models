conda create -n ebm_env_venv python=3.7

conda activate ebm_env_venv

conda install pytorch=0.4.1 torchvision=0.2.1 -c pytorch

pip install -r reuirements.txt

find scripts/ -name "*.py" -exec sed -i 's/\.cuda()//g' {} +

find data/ -name "*.py" -exec sed -i 's/\.cuda()//g' {} +