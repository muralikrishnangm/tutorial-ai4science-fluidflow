# Introduction

This repo contains tutorial of mahine learning (ML) applications in fluid flows and climate science, under the umberlla of AI for Scinece. We will start with a simple regression problem ([Example 1](#example1)) and then translate to more complex fluid flow problems ([Examples 2-4](#example2)). The ML tutorials are in IPython notebook formats, written using [Jupyter](https://jupyter.org/). JupyterLab or Google Colab is the recommended environement for running the notebooks and further development. The notebooks are meant to be used as a platform for further development, as a stepping stone. Although, the applications are for fluid flows, the problems are general regression problems which can be extended to a wide range of science fields.

Author: Muralikrishnan Gopalakrishnan Meena (Oak Ridge National Laboratory)

Contributors:
* Matt Norman (Oak Ridge National Laboratory)

## Fluid flow application

For the fluid flow application, we will formulate ML surrogate models for a subcomponent of a candidate weather simulation - [supercell test case](https://en.wikipedia.org/wiki/Supercell). Specifically, we will emulate the cloud microphysics in the simulation (temperature, water vapor, cloud water, precipitation/rain, etc.) which is traditionally solved using the [Kessler scheme](https://doi.org/10.1002/2015MS000435) and its varients. A sample 2D flow simulation of the supercell test case using the [miniWeatherML](https://github.com/mrnorman/miniWeatherML.git) app is shown below.

![supercell movie](docs/supercell_p3_2d_hires.gif "Supercell")

We will use data generated from the [miniWeatherML](https://github.com/mrnorman/miniWeatherML.git) app for training the surrogate models ([Examples 2-3](#example2)) and also deploying the ML model back to the solver ([Examples 4](#example4)). More details on the surrogate model will be discussed in the example notebooks.

# Running the notebooks

Here are some basics of running the IPython notebooks. Mainly, two environemnts are recommended:

1. [Google Colab](https://colab.research.google.com/)
2. [JupyterLab](https://github.com/jupyterlab/jupyterlab)

* To run the cells, use the different options in the `Run` option in the toolbar (at the top).

**TIP**: Use Table of Contents in the notebooks to get a big picture view of the ML training procedure. Both Google Colab and JupyterLab automatically has a Table of Content for all the cells in the notebook. Check it out on the toolbar on the left side. You can click on the sections to go to the corresponding place in the notebook.

**TIP**: You can convert the notebooks to executable scripts (Python) using [jupyter nbconvert](https://nbconvert.readthedocs.io/en/latest/usage.html#executable-script)
```
    jupyter nbconvert --to script my_notebook.ipynb
```

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

1. We start with solving a simple regression problem using Keras.
2. Next we tackle a more complex problem of forming surrogate models for emulating the non-linear behavior of fluid flow variables using Keras (solving PDEs).
3. We implemnet the above using PyTorch.
4. The above PyTorch surrogate model is coupled with the fluid flow solver.

Follow each example for more details.

## <a name="example1"></a>Example 1

* Open the notebook [0_tanh.ipynb](0_tanh.ipynb)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/muralikrishnangm/tutorial-ai4science-fluidflow/blob/main/0_tanh.ipynb)



## <a name="example2"></a>Example 2

* Open the notebook [1_miniWeatherML_supercell_NN_Keras.ipynb](1_miniWeatherML_supercell_NN_Keras.ipynb)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/muralikrishnangm/tutorial-ai4science-fluidflow/blob/main/1_miniWeatherML_supercell_NN_Keras.ipynb)



## <a name="example3"></a>Example 3

* Open the notebook [2_miniWeatherML_supercell_NN_PyTorch.ipynb](2_miniWeatherML_supercell_NN_PyTorch.ipynb)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/muralikrishnangm/tutorial-ai4science-fluidflow/blob/main/2_miniWeatherML_supercell_NN_PyTorch.ipynb)



## <a name="example4"></a>Example 4 (TBD)

* Link to sample PyTorch coupling with C++: [pytorch-cpp-example](https://github.com/muralikrishnangm/pytorch-cpp-example.git)

* Link to weather simulation solver: [miniWeatherML](https://github.com/mrnorman/miniWeatherML.git)

* Distributed Client-Server implementation: [SmartSim](https://github.com/CrayLabs/SmartSim.git)
    - Reference: Same Partee's presentation at OLCF on ["Machine Learning for HPC Simulations: Using PyTorch, TensorFlow in Fortran, C, and C++ with SmartSim"](https://www.olcf.ornl.gov/calendar/userconcall-mar2022)