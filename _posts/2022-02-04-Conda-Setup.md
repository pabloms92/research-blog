# Conda setup
> Some comments or shortcuts on how to set up your working conda environment.

Create your environment: \
``` conda create -n test-env ``` \
or \
``` conda create -n test-env python=3.7``` \
``` conda activate test-env ``` 

If you have a file with an environment setup ```environment.yml```. Use the following command to create an environment from the file: \
```conda env create -f environment.yml```

To save the current environment \
 ```conda env export > environment.yml```

To use this environment in your _jupyter-notebooks_ install the ipykernel\
``` pip install ipykernel``` \
 or \
``` conda install ipykernel -y``` \
and then install the environment in the ipykernel:\
``` python -m ipykernel install --user --name=test-env``` 


> Read more from conda [here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)

## Automation

[How to Automate Python Environment Creation (Bash)](https://towardsdatascience.com/how-to-automate-python-environment-creation-850743f1c09e)