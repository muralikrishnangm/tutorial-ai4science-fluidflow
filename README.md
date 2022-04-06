# Introduction

This repo contains tutorial of mahine learning (ML) applications in fluid flows and climate science, under the umberlla of AI for Scinece. The ML tutorials are in IPython notebook formats, written using [Jupyter](https://jupyter.org/). JupyterLab or Google Colab is the recommended environement for running the notebooks and further development. The notebooks are meant to be used as a platform for further development, as a stepping stone. Although, the applications are for fluid flows, the problems are general regression problems which can be extended to a wide range of science fields.

Author: Muralikrishnan Gopalakrishnan Meena (Oak Ridge National Laboratory)

Contributors:
* Matt Norman (Oak Ridge National Laboratory)

# Running the notebooks

Mainly, two environemnts are recommended:

1. [Google Colab](https://colab.research.google.com/)
2. [JupyterLab](https://github.com/jupyterlab/jupyterlab)

See below for details.

## Opening notebooks in Google Colab

* Lookout for the badge [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/muralikrishnangm/tutorial-ai4science-fluidflow.git) for each example. Click this badge to open the notebook in Google Colab.
* Access to notebook - should be OK when the repo is public
* Lookout for Pop-up blocker
* Need to have a Google account to run the notebook
* To save changes made, you need to save a copy in one of the following
  1. your Google Drive: `File -> Save a copy in Drive`
  2. your GitHub: `File -> Save a copy in GitHub`

## Opening in JupyterLab

The notes below are curated for a tutorial at Oak Ridge Leadership Computing Facility (OLCF). Nonetheless, a local or server version of JupyterLab would follow the same procedure.

The JupyetLab environment at OLCF can be accessed through [OLCF JupyterLab](https://jupyter.olcf.ornl.gov/). All members of currently enabled OLCF projects have access to the OLCF JupyterLab (through JupyterHub). Detailed documentation can be found [here](https://docs.olcf.ornl.gov/services_and_applications/jupyter/overview.html#jupyter-at-olcf).

* **IMPORTANT**: The OLCF JupyterLab is free to use for all members but it is a VERY limited resource. Please try your best to use Google Colab and opt for this option only if necessary.
* Sign-in using your OLCF credentials (the one used for logging in to the OLCF machines, not myOLCF).
* When selecting the options for the Labs, select the one with the GPU:
```
  Slate - GPU Lab
  JupyterLab 3 | 16 CPU | 16GB MEM | V100 GPU
```
* Clone this repo
```
  git clone git@github.com:muralikrishnangm/tutorial-ai4science-fluidflow.git
```
* Open this [README.md](README.md) file using `Markdown Preview`:
```
  [Right-click-file] -> Open With -> Markdown Preview
```
* Follow the instructions in this README file. Clicking the highlighted text for each notebook should open the notebook in a new tab. If it doesnot work, please open the notebooks directly from the file browser.

# Examples

Below are examples for getting started with ML application for general scientific problems. Here is an outline of the examples:

* We start with solving a simple regression problem using Keras.
* Next we tackle a more complex problem of forming surrogate models for emulating the non-linear behavior of fluid flow variables using Keras (solving PDEs).
* We implemnet the above using PyTorch.
* The above PyTorch surrogate model is coupled with the fluid flow solver.

Follow each example for more details.

## Example 1

* Open the notebook [0_tanh.ipynb](0_tanh.ipynb)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/muralikrishnangm/tutorial-ai4science-fluidflow/blob/main/0_tanh.ipynb)
