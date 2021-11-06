---
title: "Jupyter Notebook Trouble Shooting"

excerpt: "깃헙 블로그 포스팅 연습"
---


# Trouble Shooting

# Jupyter notebook cannot import python modules installed in a conda environment

# Why it happens?

It is because ipython kernel path is not the python path of the custom conda environment but the root python environment (or others)

# How to solve?

We have to add our custom conda environment into the ipython kernel. To do this, we need to install a package called "ipykernel". 

```bash
conda install -c anaconda ipykernel
```

Then, we have to install our conda environment into the jupyter notebook by entering following command in Linux Terminal.

```bash
python -m ipykernel install --user --name="your_env"
```

where "your_env" is the name of the conda environment you want to use in the jupyter notebook. 

After this, you can choose your env as well as the default python versions for jupyter notebook.
