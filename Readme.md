### General information 

This code belongs to the paper: Computationally Efficient and Stable Real-World EHR Synthetic Data Generation: High Similarity and Privacy Preserving Diffusion Model Approach
TabDDPM was originally developed by Akim Kotelnikov et al. the original repository can be found here: https://github.com/rotot0/tab-ddpm

This is an adaptation of the code for faster installation and plug and play synthetic data generation using TabDDPM made by myself. You can request anything by email to me at: javiagu13@gmail.com
Soon, all the experimental files will also be uploaded which include utility, similarity, privacy metrics in a plug and play way for any dataset.

### Setting up the environment for installation of TabDDPM

In order to make it clean, we are not going to install it globally but create a custom environment for TabDDPM as follows:

Open a conda prompt and type (nameofenvironment is any): 
```
conda create -n nameofenvironment python=3.9.7
```

Now you have to activate the environment
```
conda activate nameofenvironment
```

Now we have a environment with our custom name with a version of python 3.9.7 installed (your python version may vary since it will depend in the kind of GPU you may be using, pytorch, cuda, and python versions should match)


### GPU Installation

If you want to use GPU for running TabDDPM what you will need is a CUDA version that matches your card, a cuDNN and a pyTorch version that also matches both TabDDPM and the CUDA version.

In my case pytorch1.10.1, cu111, and python3.9.7 is the combination to use. Therefore, we had already installed python, now lets install CUDA:

https://developer.nvidia.com/cuda-downloads

You should look for which graphics processing unit you have and which CUDA will match it.

Once you downloaded and installed it, you should install the pytorch version that matches it (notice pytorch also installs cuDNN so you just need to find the right combination as follows):

https://pytorch.org/get-started/previous-versions/

I recommend to check the website to make sure that the version will match your CUDA but if you have the same versions as me, the following will do the trick:

```
pip install torch==1.10.1+cu111 
```

For more information on GPU installation refer to: 

https://vivek-singh.medium.com/how-to-install-tensorflow-gpu-version-with-jupyter-windows-10-in-8-easy-steps-8797547028a4

### Installing Dependencies

Finally we may also want to install the dependencies of TabDDPM, for that, simply go to the folder of TabDDPM using **cd** on anaconda prompt and run the following:

```
pip install -r requirements.txt
```


### Time To Play With Jupyter Notebook!

If you arrived here, congrats :) 

Now simply open
```
TabDDPM_Training_and_Extraction.ipynb
```

And follow the instructions.


### Extra: in case you want to run your environment in jupyter notebook

Activate your environment:
```
conda activate nameofyourenvironment
```

Install ipykernel:
```
pip install ipykernel
```

Install your environment on the kernel
```
python -m ipykernel install --user --name nameofenvironment --display-name "nameofenvironment"
```

