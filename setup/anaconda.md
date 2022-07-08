# Anaconda

Anaconda provide users with environment for scientific tools: numpy, scipy, computation engine and resource monitoring.
Anaconda supports provisioning workspace, IDE like `jupyter-notebook` and `jupyter-hub`

## Installation

**Step 1**: 

Get anaconda distribution for your OS [here](https://www.anaconda.com/products/distribution)
And move the downloaded distribution to your server location (prefer storing the distribution at `/`)


**Step 2**:

Execute the distribution file and follow its instruction. During the installation, pay attention to some options:

* Set location for anaconda3 at `/anaconda3` instead of `/root/anaconda3`. When you are prompted to make a decision, just type `/anaconda3` to set the location for the distribution.

* Choose 'yes' when being prompted to execute `conda init` after installtion


After this step, anaconda3 is sucessfully installed

**Step 3**:

Setup Anaconda3 environment variable for your OS users. 

```
# Enter password if needed
> su <username>

# Edit .bashrc file
> nano ~/.bashrc

```

Inside `~/.bashrc` add these 3 lines

```
# Anaconda
export CONDA_HOME=/anaconda3
export PATH=$PATH:$CONDA_HOME/bin
```

