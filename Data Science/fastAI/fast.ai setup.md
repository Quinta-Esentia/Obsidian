# Fast.AI Setup
https://www.youtube.com/playlist?list=PLfYUBJiXbdtSLBPJ1GMx-sQWf6iNhb8mM

## Pre-requisites
Assuming using windows:
- get windows terminal (or Powershell)
- have windows 10 updated since (march?) 2020 for wsl2.

### Setup Linux terminal in windows
*HINT!* Remeber your [[Terminal|terminal commands ;)]]
1. In (windows/powershell) terminal, enter `wsl --install` or `wsl.exe --install`
2. Make sure installation of linux kernel is complete (in our case, Ubuntu). Computer restart required. 
3. UNIX user setup required. choose user and pw
4. _optional: update linx with `sudo apt update` and `sudo apt get`_
5. setup "git" and "downloads" directories in home directory `pwd` (go with with `cd`) using `mkdir git` and `mkdir downloads`

Troubleshooting internet connectivity issues:
- https://stackoverflow.com/questions/62314789/no-internet-connection-on-wsl-ubuntu-windows-subsystem-for-linux
- https://github.com/microsoft/WSL/issues/5336#issuecomment-653881695

 

## Setup python

### Install mamba
NEW METHOD  - old method redundant [^bignote]
1. go to [fastai/fsatsetup](https://github.com/fastai/fastsetup) and get url of raw view of "setup-conda.sh" 
2. In downloads directory in terminal, use `wget https://raw.githubusercontent.com/fastai/fastsetup/master/setup-conda.sh`
3. run `bash setup-conda.sh`

4. after installation is finished, restart shell and confirm `which python` returns 
``` 
/home/*USER*/mambaforge/bin/python or something similar 
```

[^bignote]: 
	OLD method (use NEW instead)
	1. find linux installation file mamba from https://github.com/conda-forge/miniforge
	2. In downloads directory in terminal, use `wget https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-Linux-x86_64.sh`
	3. run `bash Mambaforge-Linux-x86_64.sh` and follow prompts to install mamba, choosing to initialise conda.init
	
### Reinstalling mamba
[Link to fast.ai vid](https://www.youtube.com/watch?v=56sIyFjihEc&list=PLfYUBJiXbdtSLBPJ1GMx-sQWf6iNhb8mM&index=1&t=39m50s)
If you mess up your python environment and want to start again, just 
1. remove your entire mambaforge directory with:
`rm -rf mambaforge`
2. You will also need to edit your .barshrc script that automatically runs everytime you start your termial. Use `vim .bashrc` to edit this file in [[Terminal#Vim commands|vim]],  and move to the bottom to remove everything between the `# >>> conda initialize >>>` comments.
3. Restart terminal
4. you can now cd to downloads and run `bash setup-conda.sh`

### Install jupyter
`mamba install jupyterlab`

to stop no browser warning (as none is installed in Ubuntu)
`alias jl="jupyter lab --no-browser"`

### Install pytorch
https://pytorch.org/get-started/locally/

!REMEMBER! replace `conda` with `mamba`

GPU Example:
`mamba install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch`

`conda install pytorch torchvision torchaudio cudatoolkit=11.6 -c pytorch -c conda-forge`

CPU Example:
`mamba install pytorch torchvision torchaudio cpuonly -c pytorch`

confirm installation:
1. run `ipython`
2. run `import torch`
3. run `torch.tensor(1)`
4. confirm output without errors

check if your GPU driver and CUDA is enabled and accessible by PyTorch:
`torch.cuda.is_available()`



### Install fast ai
`mamba install -c fastchan fastbook sentencepiece`

may need to install ipywidgets
`mamba install ipywidgets`

## Troubleshooting

### Enabling GPU
[Enabling GPU acceleration on Ubuntu on WSL2 with the NVIDIA CUDA Platform](https://ubuntu.com/tutorials/enabling-gpu-acceleration-on-ubuntu-on-wsl2-with-the-nvidia-cuda-platform)

- Install the appropriate Windows vGPU driver for WSL
- DO NOT NEED to install NVIDIA CUDA on Ubuntu (mamba installing pytorch will do that for us)