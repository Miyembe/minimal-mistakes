---
title: "Jupyter Notebook Kernel Addition"
excerpt: "When the python kernel for current virtual env does not appear"

categories:
  - cod
tags:
  - tips

---

I wanted to run a new experiment in a new virtualenv. However, I found that the kernel of the new environment does not appear even though I activated the virtualenv and run jupyter notebook there. 

I found that I have to add the kernel manually by running this command in terminal. 

```bash
python -m ipykernel install --user --name [virtualEnv] --display-name "[displayKernelName]"

```

Please make sure to close terminal and rerun the terminal and run jupyter notebook. I spent some time figuring out why the kernel does not appear after run this command. It was applied after I closed the terminal.

