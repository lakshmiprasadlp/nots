# Create Conda environment
```
conda create -n env python=3.9 ipykernel
```

## Activate the environment
```
conda activate env
```
## add newly created environment to the notebook as kernel
```
python -m ipykernel install --user --name=env
```
## install notebook inside the environment
```
pip install notebook
```

## Now open the notebook using below command: (from the anaconda prompt inside conda environment)
```
jupyter notebook
```
# ALL COMMANDS
```
conda create -n env python=3.9 ipykernel
conda activate env
python -m ipykernel install --user --name=env
pip install notebook
jupyter notebook

```
